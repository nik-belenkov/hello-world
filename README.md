# hello-world
# Task one: (1/998001)
from decimal import Decimal
a = Decimal('1')
b = Decimal('998001')
res = Decimal(a/b)
to_out = ''
while True:
    if a < b:
        a *= Decimal('1000')
        to_out += ' ' + str(res)[2:5]
    elif a > b:
        a = Decimal(a%b)
    res = Decimal(a/b)
    if str(res)[2:5] == '999':
        to_out += ' ' + str(res)[2:5]
        break
print(to_out)
