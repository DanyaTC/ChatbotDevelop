# ChatbotDevelop
Chatbot
Виртуальный собеседник, программа-собеседник, чат-бот (англ. chatbot) — программа, которая выясняет потребности пользователей, а затем помогает удовлетворить их. Автоматическое общение с пользователем ведется с помощью текста или голоса. Чат-бот ведет коммуникацию от лица компании или бренда с целью упростить онлайн-общение (предоставить актуальную информацию в наиболее оперативные сроки), используется как альтернатива переписке с живым оператором или звонку менеджеру компании.
## Примеры чат-ботов

Внизу приведены примеры чат-ботов, написанные на разных языках программирования, таких как Python, JavaScript и Java.

---

### Python

```python
import random

# Список приветственных фраз
greetings = ['Привет', 'Здравствуй', 'Рад тебя видеть']

# Список прощальных фраз
goodbyes = ['Пока', 'До свидания', 'Увидимся']

# Функция, которая отвечает на сообщения
def respond(message):
    if message in greetings:
        return random.choice(greetings)
    elif message in goodbyes:
        return random.choice(goodbyes)
    else:
        return "Извини, я не понимаю тебя"

# Основной цикл программы
while True:
    message = input("Ты: ")
    response = respond(message)
    print("Бот: " + response)
```

Этот чат-бот просто отвечает на приветствия и прощания случайной фразой из списка. Он использует функцию respond(), которая проверяет, является ли сообщение одной из приветственных или прощальных фраз, и возвращает соответствующий ответ. Основной цикл программы запрашивает ввод сообщения от пользователя и выводит ответ чат-бота.

---

### JavaScript

```jsx
// Список приветственных фраз
const greetings = ['Привет', 'Здравствуй', 'Рад тебя видеть'];

// Список прощальных фраз
const goodbyes = ['Пока', 'До свидания', 'Увидимся'];

// Функция, которая отвечает на сообщения
function respond(message) {
  if (greetings.includes(message)) {
    return greetings[Math.floor(Math.random() * greetings.length)];
  } else if (goodbyes.includes(message)) {
    return goodbyes[Math.floor(Math.random() * goodbyes.length)];
  } else {
    return "Извини, я не понимаю тебя";
  }
}

// Основной цикл программы
while (true) {
  let message = prompt("Ты: ");
  let response = respond(message);
  console.log("Бот: " + response);
}
```

Этот чат-бот также использует функцию respond(), чтобы проверить, является ли сообщение одной из приветственных или прощальных фраз, и возвращает соответствующий ответ. Он также использует метод includes() для проверки, содержится ли сообщение в списке приветственных или прощальных фраз. Основной цикл программы запрашивает ввод сообщения от пользователя через диалоговое окно prompt() и выводит ответ чат-бота в консоль с помощью console.log().

---

### Java

```java
import java.util.Random;
import java.util.Scanner;

public class ChatBot {
    // Список приветственных фраз
    private static final String[] greetings = {"Привет", "Здравствуй", "Рад тебя видеть"};

    // Список прощальных фраз
    private static final String[] goodbyes = {"Пока", "До свидания", "Увидимся"};

    // Функция, которая отвечает на сообщения
    private static String respond(String message) {
        if (contains(greetings, message)) {
            return greetings[new Random().nextInt(greetings.length)];
        } else if (contains(goodbyes, message)) {
            return goodbyes[new Random().nextInt(goodbyes.length)];
        } else {
            return "Извини, я не понимаю тебя";
        }
    }

    // Проверка, содержится ли элемент в массиве
    private static boolean contains(String[] array, String element) {
        for (String str : array) {
            if (str.equals(element)) {
                return true;
            }
        }
        return false;
    }

    // Основной метод программы
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Основной цикл программы
        while (true) {
            System.out.print("Ты: ");
            String message = scanner.nextLine();
            String response = respond(message);
            System.out.println("Бот: " + response);
        }
    }
}
```

Этот чат-бот также использует функцию respond(), чтобы проверить, является ли сообщение одной из приветственных или прощальных фраз, и возвращает соответствующий ответ. Он также использует метод contains() для проверки, содержится ли сообщение в списке приветственных или прощальных фраз. Основной метод программы запрашивает ввод сообщения от пользователя через Scanner и выводит ответ чат-бота в консоль с помощью System.out.println().
