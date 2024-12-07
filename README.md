# Nornickel hackathon multi model RAG with colpali
# Execution

Требования:
1. RAG пайплайн на ColPali:
   - оптимальная индексация документов
   - Проиндексировать все документы датасета
   - научиться докидывать в индекс доп документы
   - возвращать имя файла и номер страницы документа
   - научиться удалять документ из индекса
2. RAG пайплайн оптимизация:
   - возвращать саму страницу документа или несколько (функция возвращает id документов по распределению score)
   - коррекция пользовательского запроса (знаки препинания)
   - Регистр потестировать
   - управление скоростью индексации
   - управление качеством поиска
3. Пользовательское окно взаимодествия с поиском:
   - загрузить документы
   - преобразовать в pdf (если формат отличается)
   - удалить документ из индекса
   - отследить статус обучения по документу
   - Отправить запрос
   - Получить ответ поиска: название документа, страницу (или страницы) с релевантным поиском.
   - Окно ответа с генерацией LLM с конечным осмысленным ответом.
4. Аналоги ColPali пайплайна, Image to text llm
   - Исследовать аналог
   - Получить бенчмарки поиска для сравнения с ColPali
   - Генерация на основании картинки
5. Презентация и чекпойнты
   - Подготовка презентаций
   - Запись видео демо
   - Подготовка питчинга 


## Tasks

Требования:
1. **Витя** RAG пайплайн на ColPali:
   - оптимальная индексация документов
   - Проиндексировать все документы датасета
   - научиться докидывать в индекс доп документы
   - возвращать имя файла и номер страницы документа
   - научиться удалять документ из индекса
2. **Лёша.** RAG пайплайн оптимизация:
   - возвращать саму страницу документа или несколько
   - управление скоростью индексации
   - управление качеством поиска
3. **Игорь** Пользовательское окно взаимодествия с поиском:
   - загрузить документы
   - удалить документ из индекса
   - отследить статус обучения по документу
   - Отправить запрос
   - Получить ответ поиска: название документа, страницу (или страницы) с релевантным поиском.
   - Окно ответа с генерацией LLM с конечным осмысленным ответом.
4. **Артур** Аналог RAG пайплайна. Image to text LLM
   - Исследовать аналог
   - Получить бенчмарки поиска для сравнения с ColPali
   - Исследовать image to text LLM для графиков и таблиц
5. **Саша** Презентация и чекпойнты


**Ресурсы:**

1. UI

  - Opensource реализация генеративных чатов, можно взять её [https://streamlit.io](https://streamlit.io/generative-ai)
  - Вот пример готового норм [https://knowledgegpt.streamlit.app](https://knowledgegpt.streamlit.app)
  - Либо если писать самому, open Source UI комоненты можно брать отсюда [ant.design](https://ant.design)

2. ColPali

  - ColPali [About](https://huggingface.co/blog/manu/colpali)
  - Имплементация [multi_model_rag_with_colpali](https://github.com/NirDiamant/RAG_Techniques/blob/main/all_rag_techniques/multi_model_rag_with_colpali.ipynb)

3. Moondream2
   
   - Image to text LLM  [moondream2](https://huggingface.co/vikhyatk/moondream2)
5. Аналог ColPali

   - multi_model_rag_with_captioning [ipynb](https://github.com/NirDiamant/RAG_Techniques/blob/main/all_rag_techniques/multi_model_rag_with_captioning.ipynb)



**Dataset**

Ссылка на датасет с данными для обучения модели → [Скачать датасет](https://disk.yandex.ru/d/_Y0wCNLTFevIBw)

**Список вопросов для оценки**

  Первая версия

  1. Долевое участие металлов в EBITDA компании? То есть какой % EBITDA и EBITDA margin принесли продажи Ni, Cu и т д

  2. Как эта доля менялась от года к году (наверн нужно приложить отчеты хотя бы за 2-3 года)?

  3. Топ 5 факторов снижения EBITDA г/г? Также и EBITDA margin

  4. Какой актив формирует наибольшую долю FCF? Какой актив на 2 месте?

  5. Какие активы являются убыточными? Можно ли их исключить из производственной цепочки без последствий для общего цикла производства металлов?

  6. Какой прогноз по содержанию металлов руд НН на следующие 5 лет?

  7. Какую долю рынка занимает НН в производстве металлов? Как изменялась доля НН г/г? Какой прогноз на 5 лет?

  8. Как изменялся прогноз по предложению и спросу на Ni, Cu, Au в отчетах за разные года, например какой был прогноз в отчете за 2020 год на 2021/22/23? Какое было фактическое предложение и спрос в годовых отчетах 2021/22/23? Исходя из этого сделай вывод о целесообразности доверия таким прогнозам в целом

  Доп вопросы

  Годовой отчет ESG 2022

  9. Актуальная продукция НН (7 слайд)

  10. Прогноз по портфелю выручки компании на ближайшие 5 лет (16 слайд)

  11. Какие цели устойчивого развития поддержала компания? (17-18 слайд)

  Годовой отчет 2023

  12. Прогноз роста производства продукции к 2030 (9 слайд)

  13. Результаты по добычи в разбивке по регионам (9 слайд)

  14. Финансовые показатели, ебитда в абсолютах и относительных выражениях (9 слайд)

  15. Сводка по выручке от реализации металлов (45 слайд)

  16. Мультипликатор свободного денежного потока в отношении 23 к 24 году (слайд 48)

  17. Структура акционерного капитала (114 слайд)

  18. Прибыль на акцию за 21,22 и 23 годы (122 слайд)



# Main idea

**Задача:**
Документы под контролем: автоматизируй их поиск и индексацию!

Задача заключается в создании эффективного пайплайна для автоматического поиска и индексации документов с использованием мультимодального RAG и модели ColPali. Участникам предстоит разработать систему, которая сможет обрабатывать различные форматы данных, обеспечивая быструю и точную индексацию. Это решение значительно упростит доступ к информации и повысит продуктивность работы с документами в различных областях.

# 🤔 Проблематика

В современном мире объем информации, хранящейся в различных документах, постоянно растет. Организации сталкиваются с проблемами поиска, индексации и обработки данных из множества источников и форматов. Традиционные методы работы с документами часто оказываются неэффективными: они требуют значительных временных затрат на ручной поиск и анализ информации, что снижает продуктивность сотрудников и увеличивает риск ошибок.

Существующие системы поиска не всегда способны учитывать контекст и структуру документов, что приводит к недостаточной точности результатов. Использование мультимодальных подходов, таких как Retrieval-Augmented Generation (RAG), может существенно улучшить качество поиска и индексации, однако их внедрение требует создания эффективного пайплайна, который сможет обрабатывать разнообразные форматы данных и обеспечивать быструю и точную индексацию.

#  💎 Образ решения

Участникам необходимо разработать интегрированную систему, использующую мультимодальный подход RAG для автоматического поиска и индексации документов. Решение должно включать:

• Эффективный механизм индексации: система должна быть способна обрабатывать различные форматы документов (текстовые, изображения, PDF и др.) и индексировать их содержимое.

• Интуитивно понятный интерфейс поиска: пользователи должны иметь возможность легко находить нужные документы по запросам, включая поддержку семантического поиска.

• Использование модели ColPali: необходимо интегрировать эту модель в пайплайн для повышения качества поиска и индексации, учитывая контекст и структуру документов.

• Оптимизация производительности: система должна обеспечивать быструю обработку запросов и минимальное время отклика.

# 💡 Формат данных для обучения

Участникам предстоит работать с разнообразными типами данных, включая:

• Текстовые документы: документы в формате .txt, .docx, .pdf и других текстовых форматах.

• Изображения: сканированные документы, графики и диаграммы, которые могут содержать текстовую информацию.

• Мультимедийные файлы: презентации в различных форматах, которые могут потребовать TR для извлечения информации.

• Метаданные: информация о документах (дата создания, авторы, теги и т.д.), которая может быть использована для улучшения индексации.

Данные должны быть предварительно обработаны для извлечения ключевой информации, создания индексов и обеспечения возможности быстрого поиска.

# 📁 Формат загрузки решения 

**Решение должно быть представлено на платформу не позднее 10:00 МСК, 8 декабря, в следующем виде:**

1. Ссылка на исходный код в VCS (системе контроля версий - GitHub, GitLab или иные)

2. Ссылка на облачный диск (Яндекс, Google), где загружены:

  1. Архив с исходным кодом проекта

  2. Видео-демо работы проекта (видео, показывающее процесс работы вашего решения, с комментариями или без них, не длиннее 2 минут)

3. Ссылка на презентацию вашего проекта (облачный диск с файлом `.pptx`/`.pdf` или развернутая презентация на Notion, Figma или иных сервисах)

4. Ссылка на ваше развернутое решение (при наличии) для его тестирования членами жюри.

---

# 🧑‍⚖️ **Критерии оценки решений**

Будут доступны после старта хакатона.

# 🦉 Настоятельно рекомендуется

- Писать понятный код с комментариями.

- Оперативно отвечать на возможные вопросы организаторов в период код-ревью. Выделите отдельную роль в команде под это.

# ⚠️ Обратите внимание

- Обязательно при использовании внешних данных или чужого кода – указывать ссылки на первоисточник.

- Все сторонние программы, использованные в решении задачи, должны быть выпущены под лицензией, позволяющей их свободное коммерческое использование.

# 🛑 Запрещается

Помните, что любые технологии, использованные вами, должны быть официально доступны на территории РФ и обладать лицензией, позволяющей свободное коммерческое использование!

https://buildin.ai/phystech_gensis/share/dba64d1b-8af3-4447-a58e-d2095033542f



