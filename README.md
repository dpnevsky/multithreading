# Многопоточность в Java

Небольшой учебный проект с примерами и экспериментами по многопоточности в Java, созданный в **январе 2023 года**. Создан для изучения работы потоков, синхронизации и взаимодействия между задачами.

## Примеры

| Класс | Что изучается |
| --- | --- |
| [ThreadPool](src/multhreading/ThreadPool.java) | Выполнение задач в пуле потоков через `ExecutorService`. |
| [ProducerCunsumerBlockingQueue](src/multhreading/ProducerCunsumerBlockingQueue.java) | Взаимодействие производителя и потребителя через `BlockingQueue`. |
| [ProduserConsumerSynchronized](src/multhreading/ProduserConsumerSynchronized.java) | Синхронизация производителя и потребителя через `synchronized`, `wait()` и `notify()`. |
| [SynchronizedTwoLock](src/multhreading/SynchronizedTwoLock.java) | Использование отдельных блокировок для двух независимых списков. |
| [MyCountDownLatch](src/multhreading/MyCountDownLatch.java) | Эксперимент с `CountDownLatch` и уменьшением его счётчика. |

## Запуск

Требуется JDK 17 или новее. Внешние зависимости не нужны.

Каждый пример запускается отдельно через свой метод `main()` в IDE.

Для запуска из терминала выполните в корне проекта:

```bash
javac -encoding UTF-8 -d out src/module-info.java src/multhreading/*.java
java -cp out multhreading.ThreadPool
```

Для другого примера замените `ThreadPool` на имя нужного класса из таблицы.

Оба примера производителя и потребителя работают в цикле. Для остановки нажмите `Ctrl+C` или остановите программу в IDE.
