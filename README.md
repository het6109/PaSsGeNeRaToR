import random
letters = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
numbers = ["1","2","3","4","5","6","7","8","9","0"]
symbols = ["~", "!", "@", "#", "$", "%", "^", "&", "*", "(", ")", "_", "-", "+", "=", "{", "}", "[", "]", "|", ";", ":", "<", ">", "?", "/", ".", "`"]
print("Welcome to the PaSsGeNeRaToR")
input1 = int(input("How many letters do you want in your password?"))
input2 = int(input("How many numbers do you want in your password?"))
input3 = int(input("How many symbols do you want in your password?"))
sumL=0
sumN=0
sumS=0
output=0
inputT= input1+ input2+ input3
list= []
while output<inputT:
  F = random.randint(0,2)
  if F==0:
    sumL+=1
    if sumL<=input1:
      list.append(letters[random.randint(0,25)])
      output+=1
  if F==1:
    sumN+=1
    if sumN<=input2:
      list.append(numbers[random.randint(0,9)])
      output+=1
  if F==2:
    sumS+=1
    if sumL<=input1:
      list.append(symbols[random.randint(0,27)])
      output+=1
print(list)
U=""
for k in list:
  U+=str(k)
print(U)
