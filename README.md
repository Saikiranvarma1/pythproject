from datetime import datetime
name = input("Enter your name:")

#lists of items 
lists='''
 rice             Rs 20/kg
 sugar            Rs 30/kg
 salt             Rs 20/kg
 oil              Rs 80/liter
 paneer           Rs 100/kg
 maggi            Rs 50/kg
 boost            Rs 90/each
 colgate          Rs 85/each 
 '''
#declaration 

price = 0
pricelist =[]
totalprice =0
finalfinalprice =0
ilist =[]
qlist =[]
plist =[]

#rate for items 

items ={'rice':20,'sugar':30,'salt':20,'oil':80,'paneer':100,'maggi':50,'boost':90,'colgate':85}

option=int(input("For list of  items press 1:"))
if option ==1:
    print(lists)
for i in range(len(items)):
    inp1=int(input("if you want to buy press 1 or 2 for exit:"))
    if inp1==2:
        break
    if inp1==1:
        item=input("Enter your items:")
        quantity=int(input("Enter your quantity:"))
        if item in items.keys():
           price=quantity*(items[item])
           pricelist.append([item,quantity,items,price])
           totalprice=price
           ilist.append(item)
           qlist.append(quantity)
           plist.append(price)
           gst=(totalprice*5)/100
           discount=(totalprice)/15
           finalamount=gst+totalprice
           finalfinalamount=finalamount-discount
           
           print("price:",price)
           print("Gst:",gst)
           print("discount:",discount)
           

        else:
            print("sorry you entered item is not available")
    else:
       print("you entered wrong choice")
       
    inp=input("bill the items yes or no:")
    if inp=='no':
          break
    if inp=='yes':
          pass
    if finalfinalamount!=0:
       print(15*"=","sai kiran supermarket",15*"=")
       print(22*" ","Machapur",22*" ")
       print("name:",name,22*" ","date:",datetime.now())
       print(55*"_")
       print(1*" ","sno",3*" ",'items',7*"",'quantity',11*" ",'price')
    for i in range(len(pricelist)):
       print(2*" ",i,4*" ",ilist[i],8*" ",qlist[i],12*" ",plist[i])
       print(55*"_")
       print(26*" ",'Amount:','Rs',totalprice)
       print(22*" ","Gst Amount:",'Rs',gst)
       print(20*" ","Total Amount:",'Rs',finalamount)
       print(24*" ","discount:",'Rs',discount)
       print(20*" ",20*"_",5*" ")
       print(20*" ","final Amount:",'Rs',finalfinalamount)
       print(55*"_")
       print(15*" ","Thanks for visiting")
       print(55*"_")
    
