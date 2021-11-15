# python-programming #super market shopping


products=[
    {
        'id':1,
        'name':"rice",
        'price':55,
        'quantity':20
        },
    {
        'id':2,
        'name':"books",
        'price':95,
        'quantity':10
        },
    {
        'id':3,
        'name':"curd",
        'price':100,
        'quantity':5
        },
    {
        'id':4,
        'name':"drink",
        'price':110,
        'quantity':200
        },
    {
        'id':5,
        'name':"dates",
        'price':100,
        'quantity':10
        }
    ]
print("--------------------------------------------------------------")
print("\t\t Pravallika Super Market")
print("--------------------------------------------------------------")
print("Sno \t Name \t Price \t Quantity ")
print("--------------------------------------------------------------")

for product in products:
      print(product['id'],'\t',product['name'],'\t',product['price'],'\t', product['quantity'])
print("--------------------------------------------------------------")


total_bill=0
while True:    
    
    item=int(input(" Add item to cart "))
    quant=int(input(" How much: "))
    for product in products:
        if item==product['id']:
            total_bill=total_bill+product['price']*quant
    choice=input("do you want to add another item(Y - y/N - n): ")
    if choice.lower() == 'n':
        if total_bill>=3000:
            total_bill= total_bill - ( total_bill * 3/100 )
            print(" congrats, you got 3 % discount ")
        print("total Bill Amount: ",total_bill)
        break



















