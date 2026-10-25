def give_change(amount):
    coins = [50, 10, 5, 2, 1]
    result = {}
    
    for coin in coins:
        if amount >= coin:
            count = amount // coin
            amount %= coin
            result[coin] = count
            
    return result

# Пример работы программы для сдачи 87 рублей
change = give_change(87)
print("Выданная сдача:")
for coin, count in change.items():
    print(f"Монета {coin} руб.: {count} шт.")
