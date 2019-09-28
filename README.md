# Основное задание

Сделать анализ загрузки сайта lifehacker.ru в Chrome DevTools по вкладкам Network, Performance, Coverage

## Условия:

- проверить URL https://lifehacker.ru/
- использовать вкладку инкогнито с отключенными расширениями
- на вкладке Network отключить кэш (Disable cache)
- на вкладке Network
    - записать и сохранить в HAR архив профиль загрузки ресурсов при открытии страницы
    -  найти неоптимальные места:
        - дублирование ресурсов
        ![](screenshots/Screenshot_from_2019-09-28_16-07-41.png)
        ![](screenshots/Screenshot_from_2019-09-28_16-10-11.png)
        ![](screenshots/Screenshot_from_2019-09-28_16-16-12.png)
        ![](screenshots/Screenshot_from_2019-09-28_16-17-03.png)
        - лишний размер ресурса

        ![](screenshots/Screenshot_from_2019-09-28_16-43-28.png)

        суммарно transferred<resources, но видно, что для многих файлов наоборот
        ![](screenshots/Screenshot_from_2019-09-28_16-43-57.png)
        ![](screenshots/Screenshot_from_2019-09-28_16-44-16.png)
        
        - медленно загружающиеся ресурсы
        ![](screenshots/Screenshot_from_2019-09-28_16-26-14.png)
        - ресурсы, блокирующие загрузку
        ![](screenshots/Screenshot_from_2019-09-28_16-03-35.png)

- на вкладке Performance
    - записать и сохранить в файл профиль загрузки страницы
    - измерить время в миллисекундах от начала навигации до событий 
        - First Paint - 732ms
        - First Meaningful Paint -1390ms
        - DOM Content Loaded - 2080ms
        - Load - 4967ms
    - измерить, сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)
    ![](screenshots/Screenshot_from_2019-09-28_17-03-50.png)

- на вкладке Coverage
    - сохранить скриншот вкладки после загрузки страницы
    
    ![](screenshots/Screenshot_from_2019-09-28_17-10-41.png)
    
    - измерить в килобайтах объём неиспользованного CSS в ходе загрузки страницы - 228Kb
    ![](screenshots/Screenshot_from_2019-09-28_17-09-16.png)
    - измерить в килобайтах объём неиспользованного JS в ходе загрузки страницы - 2230Kb (2,4Mb-228Kb)
    ![](screenshots/Screenshot_from_2019-09-28_17-09-47.png)
