# Описание приложения "HeartCheck"

**HeartCheck** — это мобильное приложение, разработанное для оценки физической подготовки пользователей с помощью теста Руффье. Приложение предлагает интуитивно понятный интерфейс, который позволяет пользователям легко вводить свои данные и получать результаты тестирования.

## Основные функции:

- **Ввод данных**: Пользователи могут ввести свое имя и возраст, что позволяет персонализировать опыт использования приложения.
  
- **Тестирование**: Приложение проводит тесты на физическую подготовку, включая измерение пульса до и после физической нагрузки. Пользователи могут вводить результаты тестов, что позволяет отслеживать их физическое состояние.
  
- **Анализ результатов**: После завершения тестирования приложение предоставляет пользователям интерпретацию результатов, что помогает понять уровень физической подготовки и дает рекомендации по улучшению.
  
- **Анимации и визуальные эффекты**: Приложение использует анимации при переходах между экранами.

-------------------------------------------------

# Описание кода приложения "HeartCheck" main.pu

Данный код представляет собой приложение на Python с использованием фреймворка Kivy, предназначенное для оценки физической подготовки пользователей с помощью теста Руффье. Приложение имеет несколько экранов, каждый из которых выполняет определенные функции.

## Основные компоненты приложения

### 1. Импорт библиотек
Код начинается с импорта необходимых библиотек:
- `Animation` для анимации элементов интерфейса.
- `App`, `ScreenManager`, `Screen` и другие виджеты Kivy для создания графического интерфейса.

### 2. Глобальные переменные
Определены глобальные переменные:
- `age`: возраст пользователя (по умолчанию 7).
- `name`: имя пользователя (пустая строка).
- `p1`, `p2`, `p3`: переменные для хранения результатов тестов.

### 3. Классы экранов

#### `InstrScr`
- **Описание**: Экран для ввода имени и возраста пользователя.
- **Элементы**:
  - Метка с инструкцией.
  - Поля ввода для имени и возраста.
  - Кнопка для перехода к следующему экрану.
- **Методы**:
  - `next()`: сохраняет имя и переходит к экрану пульса.

#### `PulseScr`
- **Описание**: Экран для ввода результата первого теста (пульс).
- **Элементы**:
  - Метка с инструкцией.
  - Поле ввода для результата.
  - Кнопка для перехода к следующему экрану.
- **Методы**:
  - `next()`: сохраняет результат и переходит к экрану проверки приседаний.

#### `CheckSits`
- **Описание**: Экран с инструкцией по выполнению теста на приседания.
- **Элементы**:
  - Метка с инструкцией.
  - Кнопка для перехода к следующему экрану.
- **Методы**:
  - `next()`: переходит к экрану второго теста пульса.

#### `PulseScr2`
- **Описание**: Экран для ввода результатов второго теста (пульс до и после отдыха).
- **Элементы**:
  - Метка с инструкцией.
  - Поля ввода для результатов.
  - Кнопка для завершения тестирования.
- **Методы**:
  - `next()`: сохраняет результаты и переходит к экрану с результатами.

#### `Result`
- **Описание**: Экран для отображения результатов тестирования.
- **Элементы**:
  - Метка для отображения имени пользователя и результатов теста.
- **Методы**:
  - `before()`: обновляет текст метки с результатами при входе на экран.

### 4. Класс приложения `HeartCheck`
- **Метод `build()`**: создает экземпляр `ScreenManager`, добавляет все экраны и возвращает его для отображения.

### 5. Запуск приложения
В конце кода создается экземпляр приложения и запускается метод `run()`, который начинает выполнение приложения.

## Заключение
Код представляет собой простое, но функциональное приложение для оценки физической подготовки, позволяющее пользователям вводить данные и получать результаты тестирования. Интерфейс приложения интуитивно понятен и включает несколько экранов для удобства пользователя.
