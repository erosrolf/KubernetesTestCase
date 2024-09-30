# Задача:
Опишите решение для веб-приложения в kubernetes в виде yaml-манифеста. Оставляйте в коде комментарии по принятым решениям. Есть следующие вводные:

У нас kubernetes кластер, в котором пять нод.
Приложение испытывает постоянную стабильную нагрузку в течение суток без значительных колебаний. 3 пода справляются с нагрузкой.
На первые запросы приложению требуется значительно больше ресурсов CPU, в дальнейшем потребление ровное в районе 0.1 CPU. По памяти всегда “ровно” в районе 128M memory.
Приложение требует около 5-10 секунд для инициализации.
Что хотим?

Минимальное потребление ресурсов от этого deployment’а.
Размещение подов на разных нодах для отказоустойчивости.
Чтобы под не обрабатывал запросы до завершения инициализации.
