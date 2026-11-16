# Bilet-22
# 1. Введення даних
name = input("Ім'я пасажира: ")
distance = float(input("Відстань поїздки (км): "))
balance = float(input("Баланс: "))
rate = float(input("Тариф за 1 км: "))
cars = int(input("Кількість доступних автомобілів: "))
promo = input("Промокод (так/ні): ")
# 2. Логічні перевірки
# Перевіряємо, чи відстань додатна
valid_distance = distance > 0
# Перевіряємо, чи є доступні автомобілі
has_cars = cars > 0
# Перевіряємо, чи тариф додатний
valid_rate = rate > 0
# Обчислюємо вартість поїздки
cost = distance * rate
# Перевіряємо, чи балансу вистачає на поїздку
enough_money = balance >= cost
# Перевіряємо всі умови разом
can_order = (valid_distance and has_cars and valid_rate and enough_money)
# 3. Виведення результатів
print("Пасажир:", name)
print("Відстань додатна:", valid_distance)
print("Є автомобілі:", has_cars)
print("Тариф додатний:", valid_rate)
print("Достатньо коштів:", enough_money)
print("Вартість поїздки:", cost)
print("Можливість замовлення:", can_order)
# 4. Додаткові перевірки
# Перевіряємо, чи поїздка понад 30 км
long_trip = distance > 30
# Перевіряємо, чи є промокод
has_promo = promo == "так"
# Перевіряємо, чи вартість понад 500 грн
expensive_trip = cost > 500
# Перевіряємо, чи поїздка до 5 км
short_trip = distance <= 5
# Перевіряємо неможливість замовлення
cannot_order = not can_order
print("Поїздка понад 30 км:", long_trip)
print("Є промокод:", has_promo)
print("Вартість понад 500 грн:", expensive_trip)
print("Поїздка до 5 км:", short_trip)
print("Неможливість замовлення:", cannot_order)
