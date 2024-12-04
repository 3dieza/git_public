# Git Шпаргалка

Добро пожаловать в шпаргалку по Git! Здесь собраны основные команды Git, которые помогут вам начать работать с этой системой контроля версий.

## Основные команды

| Команда                             | Описание                                                               |
|-------------------------------------|------------------------------------------------------------------------|
| `git init`                          | Инициализирует новый локальный репозиторий                             |
| `git clone <url>`                   | Клонирует удалённый репозиторий на локальный компьютер                 |
| `git status`                        | Показывает статус изменений в репозитории                              |
| `git add <файл>`                    | Добавляет файл в индекс для последующего коммита                       |
| `git commit -m "сообщение"`         | Фиксирует изменения с сообщением                                       |
| `git push origin <ветка>`           | Отправляет изменения в удалённый репозиторий                           |
| `git pull`                          | Получает последние изменения из удалённого репозитория                 |
| `git branch`                        | Показывает список веток                                                |
| `git checkout <ветка>`              | Переключает на указанную ветку                                         |
| `git merge <ветка>`                 | Сливает указанную ветку в текущую                                      |
| `git remote add origin <url>`       | Добавляет удалённый репозиторий и присваивает ему имя "origin"          |
| `git log`                           | Отображает историю коммитов                                            |
| `git reset <файл>`                  | Убирает файл из индекса (до коммита)                                   |
| `git diff`                          | Показывает различия между закоммиченными и не закоммиченными файлами   |

## Основные понятия

- **Репозиторий**: Это хранилище вашего проекта, где хранятся все файлы и история изменений.
- **Коммит**: Это точка сохранения изменений в проекте. Каждому коммиту присваивается уникальный идентификатор.
- **Ветка**: Это отдельная линия разработки в проекте, которая позволяет работать над новыми функциями без влияния на основную версию.

## Работа с удалёнными репозиториями (GitHub)

1. **Создание нового репозитория на GitHub:**
   - Зайдите в GitHub, нажмите на кнопку **New repository**.
   - Создайте репозиторий с именем проекта, добавьте описание (опционально).
   
2. **Связь локального репозитория с удалённым:**
   ```bash
   git remote add origin git@github.com:ИМЯ_АККАУНТА/ИМЯ_РЕПОЗИТОРИЯ.git




___________________________________________________

Шпаргалка по Git: Хеш, лог и HEAD

Хеш коммита

	•	Что это: Уникальный идентификатор коммита в Git.
	•	Формат: Строка из 40 символов (SHA-1), состоящая из цифр 0-9 и букв a-f.
	•	Свойства:
	•	Если содержимое коммита не изменилось, хеш будет одинаковым на любых компьютерах.
	•	Любое изменение в данных приводит к совершенно новому хешу.
	•	Использование: Позволяет точно ссылаться на конкретный коммит.


Лог (История коммитов)

	•	Команда: git log
	•	Показывает подробную историю коммитов с хешами, авторами, датами и сообщениями.
	•	Сокращённый лог: git log --oneline
	•	Выводит историю в кратком виде: короткий хеш и сообщение коммита в одной строке.
	•	Навигация:
	•	Нажмите Q, чтобы выйти из просмотра лога.

HEAD

	•	Что это: Указатель на текущий коммит или ветку.
	•	Расположение: Файл HEAD в папке .git.
	•	Содержимое: Ссылка на текущую ветку, например, ref: refs/heads/master.
	•	Использование в командах:
	•	Вместо хеша последнего коммита можно использовать HEAD.
	•	Пример: git checkout HEAD переключится на последний коммит текущей ветки.


ПОЛЕЗНЫЕ КОМАНДЫ

| Команда                             | Описание                                                               |
|-------------------------------------|------------------------------------------------------------------------|
| `git show [хеш]`                    | Отображает подробную информацию о конкретном коммите                   |
| `git log --oneline`                 | Показывает историю коммитов в кратком формате                          |
| `git diff [хеш1] [хеш2]`            | Сравнивает изменения между двумя коммитами                             |
| `git checkout [хеш]`                | Переключается на указанный коммит или ветку                            |
| `git checkout HEAD`                 | Переключается на последний коммит текущей ветки                        |
| `git branch [имя_ветки]`            | Создаёт новую ветку с указанным именем                                 |
| `git checkout -b [имя_ветки]`       | Создаёт и переключается на новую ветку с указанным именем              |
| `git merge [имя_ветки]`             | Сливает указанную ветку с текущей веткой                               |
| `git remote -v`                     | Показывает удалённые репозитории, связанные с локальным                |
| `git stash`                         | Временно сохраняет изменения в рабочем каталоге                       |
| `git stash pop`                     | Восстанавливает изменения из stash                                     |
| `git reset --hard [хеш]`            | Жёстко откатывает репозиторий к указанному коммиту                     |
| `git revert [хеш]`                  | Создаёт новый коммит, отменяющий изменения указанного коммита          |
| `git reset --soft [хеш]`            | Откатывает к указанному коммиту, сохраняя изменения в индексе          |
| `git clean -f`                      | Удаляет неотслеживаемые файлы из рабочего каталога                     |
| `git remote remove <имя>`           | Удаляет связанный удалённый репозиторий                                |
| `git tag [имя_тега]`                | Создаёт тег для указанного коммита                                     |
| `git fetch`                         | Загружает изменения из удалённого репозитория, не объединяя их         |
| `git cherry-pick [хеш]`             | Применяет изменения из указанного коммита в текущую ветку              |
| `git rebase [ветка]`                | Переносит изменения текущей ветки на указанную                         |

# Git: Статусы файлов и команды для их обработки

## Основные статусы файлов в Git

| Статус          | Описание                                                                                     |
|------------------|---------------------------------------------------------------------------------------------|
| **Untracked**    | Неотслеживаемые файлы. Они созданы в рабочем каталоге, но ещё не добавлены в индекс.         |
| **Tracked**      | Отслеживаемые файлы, которые уже находятся в истории репозитория.                           |
| **Staged**       | Файлы, подготовленные к коммиту (добавлены в индекс с помощью `git add`).                   |
| **Modified**     | Изменённые файлы, которые ещё не были добавлены в индекс после изменений.                   |

---

## Типичный жизненный цикл файла в Git

1. **Создание файла:**  
   Файл только что создан и находится в состоянии **untracked**.

2. **Добавление в индекс:**  
   После выполнения команды `git add` файл переходит в состояние **staged**.

3. **Коммит:**  
   После выполнения `git commit` файл становится **tracked**.

4. **Изменение файла:**  
   Любое изменение переводит файл в состояние **modified**.

5. **Подготовка изменений:**  
   Если снова выполнить `git add`, изменения будут добавлены в индекс, и файл вернётся в состояние **staged**.

---

## Команды для работы с файлами и статусами

| Команда                     | Описание                                                                                     |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `git status`                | Показывает текущий статус файлов в рабочем каталоге и индексе.                              |
| `git add <файл>`            | Добавляет файл в индекс для подготовки к коммиту (переводит из **modified** в **staged**).   |
| `git commit -m "сообщение"` | Фиксирует изменения файлов, находящихся в индексе (переводит их в **tracked**).             |
| `git restore <файл>`        | Убирает изменения в рабочем каталоге, возвращая состояние файла к последнему коммиту.       |
| `git restore --staged <файл>` | Убирает файл из индекса, оставляя его изменения в рабочем каталоге.                        |
| `git reset HEAD <файл>`     | Убирает файл из индекса, но сохраняет изменения (аналогично `restore --staged`).            |

---

## Примеры

### Новый файл (untracked)
```bash
$ touch example.txt
$ git status
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        example.txt

# Оформление сообщений к коммитам

Сообщения к коммитам — это ключевой инструмент для описания изменений в проекте. Они позволяют быстро понять, что было изменено, зачем и каким образом. 

---

## Зачем важно писать понятные сообщения к коммитам?

- **Облегчение работы с историей проекта**: Понятные сообщения помогают быстрее находить нужные изменения.
- **Улучшение командной работы**: Сообщения служат инструментом коммуникации между разработчиками.
- **Обеспечение стандартов качества**: Соблюдение правил оформления делает историю коммитов читаемой и последовательной.

---

## Примеры сообщений

### Информативные сообщения

- Исправлена ошибка #123 для пользователей без отчества
- Оптимизирована загрузка фотографий в галерее
- Добавлена сортировка по полю «Сумма»
- Кнопка «Выход» сделана красной

### Неинформативные сообщения

- Новые кнопки
- Ещё фиксы
- Разные оптимизации
- Лёхины вчерашние изменения, он в отпуске

---

## Рекомендации по написанию сообщений

1. **Сообщение должно быть коротким и информативным**:  
   Сообщения должны вмещаться в 72 символа, чтобы быть читаемыми в логах.
   
2. **Используйте активный глагол**:  
   Для русскоязычных сообщений используйте инфинитив («добавить», «исправить»).  
   Для англоязычных сообщений — повелительное наклонение (imperative, например, "Fix", "Add", "Update").

3. **Структура сообщения**:  
   Укажите, что было сделано, где и зачем.  
   Пример:  
   - Исправить повторную отправку заказов  
   - Fix #303, update bluelib dependency to version 4

---

## Популярные стили оформления

### Корпоративный стиль

Сообщения включают идентификатор задачи из системы управления проектами, например Jira:  
```bash
git commit -m "LGS-239: Дополнить список пасхалок новыми числами"