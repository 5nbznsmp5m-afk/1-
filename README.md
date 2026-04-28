🛠 План розробки проєкту: [Камінь-Ножиці-Папір 2.0]

1. Концепція продукту
  
  Тип додатку: Десктоп (Консольна гра)
  Основна ідея: Розширена версія класичної гри "Камінь-Ножиці-Папір" з 15 предметами. Гравець обирає предмет за допомогою стрілок і пробілу,        комп'ютер випадково обирає свій. Кожен предмет перемагає 7 інших за заданими правилами. Гра визначає переможця та показує результат.
  
2. Основний функціонал (Features)

  Відображати меню з 15 предметами для вибору
  Навігація стрілками вгору/вниз по списку предметів
  Підтвердження вибору клавішею ПРОБІЛ
  Комп'ютер випадково обирає предмет
  Визначення переможця за правилами (хто кого б'є)
  Відображення результату (гравець vs комп'ютер)
  Таблиця правил за клавішею H
  Вихід з гри за клавішею Q
  
3. Структура даних

Назва змінної	Тип даних	Для чого потрібна
Назва змінної       | Тип даних             | Для чого потрібна
--------------------|-----------------------|----------------------------------------
ITEMS               | list[str]             | Список усіх 15 предметів
RULES               | dict[str, list[str]]  | Правила: кожен предмет -> кого б'є
pressed_key         | str / None            | Натиснута клавіша
selected_index      | int                   | Індекс вибраного предмета в меню
game_state          | str                   | Стан гри: "menu", "result", "rules"
computer_choice     | str / None            | Предмет, обраний комп'ютером
result_message      | str                   | Повідомлення про результат
player_choice       | str / None            | Предмет, обраний гравцем
Константи (не змінюються під час роботи):

Назва константи	Тип	Значення	Призначення

Назва константи     | Тип    | Значення                    | Призначення
--------------------|--------|-----------------------------|-----------------------------
ITEMS               | list   | ["Камінь", "Пістолет", ...] | Список усіх 15 предметів
RULES               | dict   | {"Камінь": ["Ножиці", ...]} | Правила: хто кого б'є

## 4. Архітектура та Дизайн
 - 🗺️ **Схема логіки:** [https://mermaid.live/edit#pako:eNqlk21P01AUx7_KzeVtwbu1XVljMKyjPLwj8ZXdYiprB7FrSddGcVvCQ4K-MEIwgIoPiImvjGEL6DJgfIVzv5Gnt1VHIq9cstuenv_5nfM_3Vp0Kag5VKeuFzxZWrbDiNwvV3yCn2kLPsMJ7MIxnNx9FN6ZgkM4hWu-xTdgQOAahnwThjDgWwQGcIG5Hj_gL6pkfHyKlCx4DR_hCL978AHewFsCX_HyDo6qKb4kdEarbjech83Ijpx7nTSTnkaSbzccP26TsgXvYR8539NB9qAPXWy2jmPwdTiHM7iEcxzntDpaHDrN2IvaZMZCD_s4_hcc6JvwlDn6lBjAyX_CKVb3E1fnAniJiR98m-_cBMae02wT08LCY6TsoaMj2P03KxkHuriYPnJeVUe9lYX3WQu308V2Q5Rh5Y016gLKN_gmX-cH-HwAfSm1O0y8w4VE5iSymHFnBHEOifw5JvGlQA9RV3DFd9LxuvjojL8c5zuIGvLDG934QcYxBWf-vznpOStoC5bYTU-s9gqXK2gEeoRv44vE8qxoLpWnwfxokJ4L6U-r4qdhM1rzHDJN3BXP08cUY9pUmbQUeEGoj7muOyoqZaJ8rlgw5VtERiYyzeIk-0NijI2KypmoaOS10m3tZjKRqyiyXLhFZGYixkpGWRlpRyVaD1dqVI_C2JFowwkbdhLSVlJeodGy03AqVMfbmh0-rtCK38GaVdt_EASN32VhENeXqe7aXhOjeLWG_7Dyil0P7b8Sx685oRHEfkR1VRCo3qJPqZ7XChOMFWWZyYVJPPOaRNeoXmATal5lTFXk3KSsFhS1I9Fnoimb0NRijmlKjhWZpimq0vkFBCHjWg]
 - 🎨 **Дизайн:** Консольна гра
