# Bojan Ivanovski 225014


# Control Flow Graph
<img src="Control Flow Graph.png" width="100%" height="auto">


# Цикломатска Kомплексност
Цикломатска комплексност е **10** според формулата:
	**E - N + 2P**
Имаме 31 ребро, 23 јазли и 1 компонента.
Исто така имаме 9 предикатни јазли или имаме 10 региони.
Е = 31 ребра
N = 23 јазли
P = 1 компонента

# Тест Случаи (Every Branch)

1. AllItems = `null` and Payment = ANY -> throws Exception
2. AllItems = `[];` and Payment = 0; -> returns True : Бидејќи е празна листата тоа значи дека sum ке биде 0 : sum <= 0
3. AllItems = `[];` and Payment = -1; -> returns False : Бидејќи е празна листата тоа значи дека sum ке биде 0 : sum <= -1
4. AllItems = `[{name = "", barcode = null, price = "40", discount = 0}];` and Payment = ANY -> throws Exception
5. AllItems = `[{name = "", barcode = "012345", price = "300", discount = 0.5}];` and Payment = 150 -> returns True : 150 <= 150
6. AllItems = `[{name = "", barcode = "012345", price = "300", discount = 0.5}];` and Payment = 100 -> returns False : 150 <= 100
7. AllItems = `[{name = "Name", barcode = "ABC123", price = "127", discount = 0}];` and Payment = ANY -> throws Exception
8. AllItems = `[{name = "Name", barcode = "098765", price = "30", discount = -1}];` and Payment = 30 -> returns True : 30 <= 30 : Попустот не се брои дека е помал од 0
9. AllItems = `[{name = "Name", barcode = "098765", price = "30", discount = -1}];` and Payment = 10 -> returns False : 30 <= 10 : Попустот не се брои дека е помал од 0


# Тест Случаи (Multiple Condition)
1. AllItems = `price = 500, discount = 1, barcode = "0"` and Payment = 460 -> returns False : 500 <= 460
2. AllItems = `price = 600, discount = 1, barcode = "0"` and Payment = 500 -> returns False : 500 <= 600
3. AllItems = `price = 500, discount = 0, barcode = "0"` and Payment = 500 -> returns True : 500 <= 500
4. AllItems = `price = 500, discount = 1, barcode = "1"` and Payment = 500 -> returns True : 500 <= 500

