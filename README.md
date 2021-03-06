В этом репозитории находятся материалы тестового задания по вёрстке для шестой [Школы разработки интерфейсов](https://academy.yandex.ru/events/frontend/shri_msk-2018).

**Макеты:**

- [десктоп](desktop-images)
- [мобильные телефоны](touch-images)

**Спецификация:**

- [десктоп](desktop-guide)
- [мобильные телефоны](touch-guide)


**TЗ на вёрстку**
Мы хотим проверить, насколько хорошо вы умеете верстать и знаете особенности браузеров. Предлагаем вам сверстать две страницы для сервиса бронирования переговорок из первого задания.

Задание
Нужно сверстать страницу списка переговрок и форму редактирования встречи. Для каждой страницы дизайнер подготовил макет (отдельно для большого экрана и мобильных телефонов).

Макет (просмотр)
Репозиторий на GitHub (скачивание файлов)

Важно сверстать страницы в точном соответствии с макетами. Если какие-то части макетов покажутся вам непонятными, обязательно задавайте уточняющие вопросы — пишите на адрес frontendschool@yandex-team.ru.
Страница списка переговорок

В шапке отображается логотип сервиса и кнопка «Создать встречу».
Слева отображается список переговорок с разбивкой по этажам.
Справа от списка отображается диаграмма встреч.
При клике на встречу всплывает тултип с информацией о ней.
При наведении на свободное время появляется кнопка добавления встречи и подсвечивается название комнаты.
Названия переговорок, у которых не осталось свободных периодов времени, отображаются менее контрастно.
На диаграмме вертикальной линией показано текущее время.
Сверху от списка отображается текущая дата и кнопки перехода к соседним датам.
При клике на текущую дату отображается календарь на три месяца.
Макет календаря дизайнер не нарисовал, сверстайте этот блок на своё усмотрение.
Страница редактирования встречи

Есть возможность ввести название встречи, дату и время начала и окончания встречи, выбрать участников и переговорку.
Выпадающий календарь для поля выбора даты делать необязательно, но это будет плюсом.
Участники встречи выбираются из списка, который появляется, когда пользователь переходит на поле поиска сотрудника.
Выбранные участники отображаются под полем ввода.
Если переговорка не выбрана, отображается список доступных комнат.
Если переговорка выбрана, то вместо списка отображается только она (с возможностью отменить выбор).
Критерии
В первую очередь мы будем проверять, свёрстаны ли страницы в точном в соответствии с макетами.
Всё должно работать в двух последних версиях Google Chrome, Яндекс.Браузера, Microsoft Edge, Mozilla Firefox, Safari, Opera. По возможности используйте приёмы безопасной деградации CSS.

Уделите внимание организации и оформлению кода. Оптимизация производительности и автоматизация будут плюсом.

**Задание на JS**
В первом задании вы подготовили бэкенд, во втором — вёрстку. Цель третьего задания — реализовать одностраничное приложение «Яндекс Переговорки», которое будет использовать все наработки из предыдущих заданий. Приложение должно обладать всей функциональностью, изображённой на макете из второго задания.

Необходимо реализовать следующие переходы между макетами:

При клике по свободному «слоту» в списке переговорок происходит переход на форму создания встречи с заполненным временем проведения и названием переговорки; если пользователь меняет время, выбранная переговорка заменяется на блок рекомендаций — о нём ниже.
При клике по кнопке «Создать встречу» также происходит переход на форму создания встречи, но без заполненных полей (блок рекомендаций отсутствует и появляется только после ввода времени проведения встречи).
Для блока рекомендаций необходимо реализовать функцию getRecommendation (описание интерфейса), которая будет подбирать подходящие переговорки для встречи, учитывая:

количество участников и вместимость переговорок;
близость переговорки ко всем участникам встречи (первыми в списке должны быть переговорки, для которых суммарное количество пройдённых всеми участниками этажей будет минимальным).
Если все подходящие переговорки заняты, необходимо проверить, возможно ли освободить какую-то из них: а) Может быть, можно перенести встречу из неё в другую переговорку (например, меньших размеров). б) Если переговорки заняты не на весь период времени, стоит попробовать освободить одну из них, перенеся встречи в другие подходящие переговорки. Например, есть встреча с 11:00 до 12:00 и есть две подходящие переговорки А (занята с 11:00 до 11:30) и B (занята c 11:30 до 12:00). В таком случае можно перенести получасовую встречу из A в B, чтобы освободить А, или перенести встречу из B в A, чтобы освободить B. Вариант выбираем так, чтобы суммарное количество пройдённых всеми участниками этажей было минимальным.

Если не удалось найти никаких вариантов, необходимо выбрать подходящие переговорки, которые освободятся раньше других.

Всевозможные сценарии обработки некорректных данных, введённых пользователем, и системных ошибок, не описанных во втором задании, мы предлагаем продумать самостоятельно и спроектировать в качестве необязательного задания.

Мы не ограничиваем вас в выборе технологий, фреймворков и библиотек. Пожалуйста, для каждого выбранного инструмента напишите небольшое обоснование — зачем он нужен в вашем проекте и почему именно он.

Мы будем оценивать реализацию функциональности, а также:

оформление кода;
архитектуру приложения;
организованную вами инфраструктуру для разработки;
наличие и качество тестов;
performance.
