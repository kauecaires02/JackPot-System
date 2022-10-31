# JackPot-System
    if RENDA > 15000:       print("Autorized")     else:       print("Nop")
    import random

#inicio com 50$
     
    credito = 50
    jogar = True
    frutas = ["laranja","abacaxi","morango","uva","banana","melancia"]
     
    while jogar:
      
      m1 = random.choice(frutas)
      m2 = random.choice(frutas)
      m3 = random.choice(frutas)
      
      print("Creditos:",credito)
      print("--------------------")
      print(m1,m2,m3)
      print("--------------------")
     
      if m1 == m2 and m2 == m3:
        print("Yeah +R$10,00")
        credito+=10
      elif (m1 == m2 or m2 == m3) and m1 <> m3:
        print("P Very nice +R$2,00")
        credito+=2
      else:
        print("GoodLuck-R$1,00")
        credito-=1
        
      if credito <= 0 or input("Deseja jogar mais uma rodada S/N?") not in "Ss":
        jogar = False
     
    print("Finish")
    print("Total-->",credito)
