# Campus Item Borrowing System \&amp; MinHeap Implementation



## Introduction

This project contains two core programming tasks:

- **TASK1**: Campus Item Borrowing Management System, implementing core functions including item borrowing, return, and record query\.

- **TASK2**: MinHeap data structure implementation and heap sort algorithm, demonstrating core heap operations and sorting applications\.

## :book: Contents

- \[TASK1 Campus Item Borrowing System\]\(\#task1\)

    - \[Features\]\(\#task1\-feature\)

    - \[Quick Start\]\(\#task1\-quick\)

    - \[Core Code Explanation\]\(\#task1\-code\)

- \[TASK2 MinHeap \&amp; Heap Sort\]\(\#task2\)

    - \[Basic Concepts\]\(\#task2\-concept\)

    - \[Quick Start\]\(\#task2\-quick\)

    - \[Core Code Explanation\]\(\#task2\-code\)

- \[Contact\]\(\#contact\)

## :books: TASK1 Campus Item Borrowing System

### :sparkles: Features

The campus item borrowing system supports these core functions:

1. View all items with status \(available/borrowed\)

2. Borrow items \(user/item validation \+ status check\)

3. Return items \(status validation\)

4. View all borrowing/return records

### :flight\_departure: Quick Start

#### Requirements

- Python 3\.7 or higher

#### Steps

1. Ensure the file structure:

    ```Plain Text
    ├── borrow_system.py
    ├── user.py
    ├── item.py
    └── main.py
    ```

2. Run the main program:

    ```shell
    python main.py
    ```

3. Follow the menu instructions in the terminal\.

### :code: Core Code Explanation

|File|Main Class|Key Function|
|---|---|---|
|`user\.py`|`User`/`Admin`|Defines user ID, name, and permission|
|`item\.py`|`Item`|Manages item status and borrow/return logic|
|`borrow\_system\.py`|`BorrowSystem`|Controls business logic and records logs|
|`main\.py`|\-|Provides interactive CLI interface|

#### Example Logic

```python
def borrow_item(self, user_id, item_id):
    user = self.users.get(user_id)
    item = self.items.get(item_id)
    if not user or not item:
        return False, "User/Item doesn't exist"
    if item.borrow_item(user_id):
        self.records.append(f"{user_id} borrow {item_id}")
        return True, "Borrowing Successfully"
    return False, "Item has been borrowed"
```

## :computer: TASK2 MinHeap \&amp; Heap Sort

### :bookmark\_tabs: Basic Concepts

- **MinHeap**: A complete binary tree where each parent node is less than or equal to its children\.

- **Root**: Always the minimum value\.

- **Core operations**: insert, extract min, heapify up/down, heap sort\.

### :flight\_departure: Quick Start

#### Requirements

- Python 3\.7 or higher

#### Steps

1. Run the heap implementation:

    ```shell
    python heap_study.py
    ```

2. View the sorted output\.

### :code: Core Code Explanation

|Class/Function|Method|Description|
|---|---|---|
|`MinHeap`|`parent/left/right child`|Calculate node indices|
|`MinHeap`|`insert`|Insert element and maintain heap|
|`MinHeap`|`extract\_min`|Remove and return minimum value|
|`heap\_sort`|\-|Sort array in O\(n log n\) time|

#### Example Logic

```python
def heapify_down(self, i):
    smallest = i
    left = self.left_child(i)
    right = self.right_child(i)
    if left < len(self.heap) and self.heap[left] < self.heap[smallest]:
        smallest = left
    if right < len(self.heap) and self.heap[right] < self.heap[smallest]:
        smallest = right
    if smallest != i:
        self.heap[i], self.heap[smallest] = self.heap[smallest], self.heap[i]
        self.heapify_down(smallest)
```

## :email: Contact

For questions or suggestions:

- Email: [example@mail\.com](mailto:example@mail.com)

- GitHub: [your\-repo\-url](https://github.com/)

## Disclaimer

This project is for **educational purposes only**\. Not for commercial use\.

> （注：文档部分内容可能由 AI 生成）
