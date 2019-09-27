f=open("lyrics.txt","r")
tx=""
for i in f:
    tx=tx+i
	
print(tx)
want_space=input('do you want to include spaces in shingles?')
if want_space == "no":
    tx=tx.replace(" ","")


k=int(input("Enter k: "))
l_for_tx=len(tx)
print(l_for_tx)
l=[]
for z in range(0,l_for_tx):
    if (z+k)>=l_for_tx:
        break
    else:
        #print(z,k)
        l.append(tx[z:z+k])
        print(tx[z:z+k])
		
		
print(l)


    