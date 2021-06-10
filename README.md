## Асинхронность (RxJS)
Есть три потока:
1. `clearFields$` - очищает все поля  
2. `getInputTextOnChange$` - возвращает текст поля ввода, если оно изменяется  
3. `getApiPromiseOnInputChange$` - возвращает промис на результат запроса к API  
Функции `resolveCancelRequest()` и `resolveRaceCondition()` подписываются на `getApiPromiseOnInputChange$`, а не сами обращаются к api, это сделано для того, чтобы снизить количество запросов на "сервер".  
Реализацию можно посмотреть в файле (index.html)[./index.html], a работу скрипта на (странице GitHub Pages)[https://cergmin.github.io/rxjs-shri-homework/].