# Python Variables and format

### 1. 1 Variables

* Variables? : 데이터를 호출하기 쉽게 임시 저장 공간(메모리)에 저장, 저장 공간의 이름을  Variables라고 한다.

```python
[변수명] = [data]
```

* 변수의 선언
  * 변수명은 문자, 숫자, '_'를 사용하여 선언한다.
  * 숫자로 시작하는 변수명은 선언할 수 없다.
  * 대/소문자를 구분한다.
  * 공백을 포함할 수 없다.



### 1.2 자료형

* **LIST** : Lists are used to store multiple items in a single variable

  * List items are **ordered**, **changeable**, and **allow duplicates values**

    * ordered(순서가있는)  :   add new items to a list, the new items will be placed at the end of the 

      list * tip : list의 순서를 변경 할 수 있는 list method가 있으나, 일반적으로 list 안의  item의 순서를

    ​       변경하지 않는다.

    * changeable : list를 선언하고 나서, 변경, 추가, 삭제가 가능
    * Allow Duplicates : index값을 참조하여, 같은 value값을 가져올 수 있다.

  * **list length & items data types**

    * ```
      list_data = [1,2,3, (1,2), "apple"]
      len(list_data) >> 변수의 길이 측정
      ```

    * ```
      item_data_type = ["Strings", nubmer, bools, tuple, dictionary,
      	   			etc(can be of data type)]
      ```

  * **list 선언**

    * ```
      list_data = list(())
      ```

    * ```
      list_name = [items or ' ']
      ```

  * **list method**

    * ```
      1. insert()
      data_list = ["apple", "banna", "cherry"]
      data_list.insert(2, "strawberry")
      print(data_list)
      ["apple", "banna", "strawberry", "cherry"]
      ```

    * ```
      2. append()
      data_list = ["apple", "banna", "cherry"]
      data_list.append("strawberry")
      print(data_list)
      ["apple", "banna", "cherry", "strawberry"]
      ```

    * ```
      3. extend()
      data_list = ["apple", "banna", "cherry"]
      data_list2 = ["watermelon"]
      data_list.extend(data_list2)
      print(data_list)
      ["apple", "banna", "cherry", "watermelon"]
      ```

    * ```
      4. remove()
      data_list = ["apple", "banna", "cherry"]
      data_list.remove(1)
      print(data_list)
      data_list = ["apple", "cherry"]
      ```

    * ```
      5. pop()
      data_list = ["apple", "banna", "cherry"]
      data_list.pop()
      ["cherry"]
      print(data_list)
      data_list = ["apple", "banna"]
      * pop() method removes the last time
      ```

    * ```
      6. del
      del [list_name]
      ```

    * ```
      7. clear()
      data_list = ["apple", "banna", "cherry"]
      data_list.clear()
      []
      ```

  * **Indexing**

    * ```
      1. list 첫 번째 item 접근
      data_list = ["apple", "banana", "cherry"]
      data_list[0] = [apple], data_list[1] = [banana], data_list[2] = [cherry] 
      ```

    * ```
      2. Negative indexing
      data_list = ["apple", "banana", "cherry"]
      data_list[-1] = ["cherry"]
      data_list[-3] = ["apple"]
      ```

    * ```
      3. Range of Indexes
      data_list = ["apple", "banana", "cherry", "kiwi", "melon"]
      data_list[:] = ["apple", "banana", "cherry", "kiwi", "melon"]
      data_list[1:] = ["banana", "cherry", "kiwi", "melon"]
      data_list[2:4] = ["cherry", "kiwi"]
      ```

    * ```
      4. Change a Range of Item Values
      data_list = ["apple", "banana", "cherry", "kiwi", "melon"]
      data_list[1:3] = ["water_melon", "strawberry"]
      print(data_list)
      ['apple', 'water_melon', 'strawberry', 'kiwi', 'melon']
      ```

    * ```
      5. Change the second and third value by replacing it with one value
      data_list = ["apple", "banana", "cherry"]
      data_list[1:3] = ["watermelon"]
      print(data_list)
      data_list = ["apple", "watermelon"]
      ```

* **Tuple** : Lists are used to store multiple items in a single variable

  * A tuple is a collection which is ordered and **unchangeable**

    * unchangeable : we cannot change, add , remove items after the tuple has been created
    * Allow Duplicates : index값을 참조하여, 같은 value값을 가져올 수 있다.

  * tuple length & item data types

    * ```
      tuple_data = (1,2,3,4)
      len(tuple_data)
      ```

  * tuple 선언

    * ```
      with one item
      tuple_data1 = ("annie",) // ' , '을 빠뜨리지 말자, 빼면 str으로 선언됨..
      ```

    * ```
      with numberable items
      tuple_data2 = (1,2,3,4, "apple", "banna", {1:10})
      ```

  * Indexing

    * ```
      
      ```

    * ```
      
      ```

    * ```
      
      ```

    * 

  * 

* **Set** : Lists are used to store multiple items in a single variable

  * A set is a collection which is both **unordered** and **unindexed**

    * unordered & unindexed items

      * ```
        set_data = {"mary", "john", "james"}
        * 순서가 없거나, 인덱싱되지 않은 item들을 set으로 선언하면 random으로 출력된다.
        ```

  *  Set items are unordered, unchangeable, and do not allow duplicate values.

    * Do not allow duplicate values

      * ```
        set_data = { "mary", "john", "james", "john"}
        print(set_data)
        {"mary", "john", "james"}
        ```

data = {
    "name": {
        "age": {
            "address": 35
        }
    }
}
data["name"]["age"]["address"



x = {'a': 1, 'b': 2}
y = {'b': 10, 'c': 11}
x.update(y)
x.copy()