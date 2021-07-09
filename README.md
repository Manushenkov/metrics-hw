Статы выводятся в консоль странички getdata.html

На страничке, помимо изначально данных нам метрик, собираются данные о: <br/><br/>
платформе - touch/desktop <br/><br/>
Браузере <br/><br/>
Ширине/высоте экрана <br/><br/>
Количестве поизведенных кликов для текущей сессии(хранится в sessionStorage.clickcount) и ID сессии (sessionStorage.id). Данные отправляются при закрытии страницы <br/><br/><br/>

На страничке getdata.html, помимо изначально данной нам функции calcMetricByDate, есть ф-ии: <br/><br/>
compareMetric(data, page, name, date1, date2) - сравнивает дни date1 и date2 по метрике name <br/><br/>
showPlatformStatsPeriod(data, required, startDate, endDate = false) - выводит статистику по метрике required (в нашем случае browser или platform) по состоянию на 
день startDate если endDate не указан, иначе в отрезке от startDate до endDate <br/><br/>
showSessionStorage(data, sessionId, isAll = false) - выводит (последний, если ничего не передавать третьим аргументом, все, если передать true) sessionStorage.clickcount для сессии с заданным SessionId <br/><br/>
showSessionMetrics(data, sessionId) - выводит все метрики, собранные в сессии с указанным sessionId<br/><br/>
showMetricByPeriod(data, page, name, startDate, endDate) - выводит метрики name с отрезке от startDate по endDate
