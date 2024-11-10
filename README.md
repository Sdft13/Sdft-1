Вот упрощённый вариант калькулятора, в котором все результаты выводятся одной строкой:

def calculator(operation):
    def wrapper(a, b):
        if operation == "add":
            return a + b
        elif operation == "subtract":
            return a - b
        elif operation == "multiply":
            return a * b
        elif operation == "divide":
            return "Ошибка: деление на ноль" if b == 0 else a / b
    return wrapper

@calculator("add")
def add(a, b):
    pass

@calculator("subtract")
def subtract(a, b):
    pass

@calculator("multiply")
def multiply(a, b):
    pass

@calculator("divide")
def divide(a, b):
    pass

# Вывод всех результатов одним принтом
results = [
    add(10, 5),         # Сложение: 15
    subtract(10, 5),    # Вычитание: 5
    multiply(10, 5),    # Умножение: 50
    divide(10, 5),      # Деление: 2.0
    divide(10, 0)       # Ошибка: деление на ноль
]

print(*results, sep=", ")

Объяснение

Результаты всех операций сохраняются в список results.

print(*results, sep=", ") выводит все значения списка через запятую в одной строке.


