- 👋 Hi, I’m @akashiminato
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

bd=["Telefonou para a vítima?","Esteve no local do crime?","Mora perto da vítima?","Devia para a vítima?"
,"Já trabalhou com a vítima?"]
rp = []
total = 0
def case(z):
    for i in z:
        if ord(i) > ord('Z'):
            z = chr(ord(i)-32)
            return z
        return z
            
for i in range(5):
    print(bd[(i)])
    x = input('S = Sim | N = Não: ')
    if case(x) == "N" or case(x) == "S":
        rp.append(case(x))
    else:
        print('Entrada Inválida.Tente Novamente.')
        while True:
            x = input('S = Sim | N = Não: ')
            if case(x) == "N" or case(x) == "S":
                rp.append(case(x))
                break
            else:
                print('Entrada Inválida.Tente Novamente.')
if rp.count('S') == 5:
        print("Assassino.")
elif rp.count('S') > 2:
        print('Cúmplice.')
elif rp.count('S') == 2:
        print('Suspeito.')
else:
        print('Inocente.')
