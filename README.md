# JmeterSamplers
JmeterSamples - примеры скриптов для нагрузочного тестирвоания на примере сайта reqres.in

Описание тестов:
1. GetVarFromJSON_ForEachController.jmx - перебор всех значений из массива, полученого в JSON-response
- в http запросе получаем JSON
- парсим из него все значения email
- в цикле FOREACH перебираем все полученные email

2. ReadDataFromJSON.jmx - чтение данных из ответа JSON в JSONObject в JSR223 PostProcessor на JAVA
Примечание: на всякий случай если не будет работать reqres.in, ответ JSON, который используется в этом примере есть в файле listColor.json

3. Loop+Counter.jmx - 2 цикла - внешний External и вложенный Nested. Внутри них реализован счетчик по вложенному циклу:
- во внешнем цикле счетчик устанавливается в переменную Jmeter = 1.
- во вложенном цикле счетчик переменная счетчика с помощью JSR223 Sampler на Java увеличивается на 1.
Такая структура нужна потому что стандартный счетчик Jmeter Counter при работе в 2-ух циклах (внешний+вложенный) не сбрасывается на начальное значение внутри вложенного цикла. То есть если внешний цикл до 10 и вложенный до 10, то Counter в конце будет 100!
Поэтому и нужен счетчик на Java.
