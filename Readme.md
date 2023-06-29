# Описание разворота связного списка

Это простой Java код для разворота связного списка. Связный список представляет собой структуру данных, состоящую из узлов, где каждый узел содержит значение (`val`) и ссылку на следующий узел (`next`).

## Описание классов

### `ListNode`:

Класс `ListNode` представляет узел связного списка. Он содержит два поля: `val` для хранения значения узла и `next` для ссылки на следующий узел.

### `LinkedListReversal`:

Класс `LinkedListReversal` содержит метод `reverse`, который принимает голову связного списка и разворачивает его. Метод использует итеративный подход, где он меняет ссылки между узлами, чтобы список стал развернутым. Результатом работы метода является новая голова развернутого списка, которая возвращается из метода.

### `Main`:

В классе `Main` содержится метод `main`, который является точкой входа в программу. В нем создается связный список с несколькими узлами, выводится исходный список, вызывается метод `reverse` для разворота списка, и затем выводится развернутый список.

## Пример использования

```java
public class Main {
    public static void main(String[] args) {
        // Создаем список: 1 -> 24 -> 35 -> 34 -> null
        ListNode head = new ListNode(1);
        ListNode second = new ListNode(24);
        ListNode third = new ListNode(35);
        ListNode fourth = new ListNode(34);

        head.next = second;
        second.next = third;
        third.next = fourth;

        // Выводим исходный список
        printList(head);

        // Разворачиваем список
        LinkedListReversal reversal = new LinkedListReversal();
        ListNode reversedHead = reversal.reverse(head);

        // Выводим развернутый список
        printList(reversedHead);
    }

    public static void printList(ListNode head) {
        ListNode curr = head;

        while (curr != null) {
            System.out.print(curr.val + " -> ");
            curr = curr.next;
        }

        System.out.println("null");
    }
}
```

В данном примере создается связный список `1 -> 24 -> 35 -> 34 -> null`, затем метод `reverse` класса `LinkedListReversal` используется для разворота списка. Результатом является развернутый список `34 -> 35 -> 24 -> 1 -> null`, который выводится на экран.кими узлами, выводится исходный список, вызывается метод reverse для разворота списка, и затем выводится развернутый список.