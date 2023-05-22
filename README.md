# JmeterSamplers
JmeterSamples - примеры скриптов для нагрузочного тестирвоания на примере сайта reqres.in

Описание тестов:
1. GetVarFromJSON_ForEachController.jmx - перебор всех значений из массива, полученого в JSON-response
- в http запросе получаем JSON
- парсим из него все значения email
- в цикле FOREACH перебираем все полученные email

2. ReadDataFromJSON.jmx - чтение данных из ответа JSON в JSONObject в JSR223 PostProcessor на JAVA
Примечание: на всякий случай если не будет работать reqres.in, ответ JSON, который используется в этом примере есть в файле listColor.json
