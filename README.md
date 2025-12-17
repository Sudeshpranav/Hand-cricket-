import random as rd
user=input('Enter your name : ')
toss_user=int(input("Enter 1 for Tails and 0 for Heads : "))
toss=rd.randint(0,100)
toss=toss%2
mat=0
print('Range starts from 0 to 6  and if it exceeds the limit then the ball is not considered')
if(toss==toss_user):
    print("You have won the toss")
    choose=int(input("Enter 1 for batting and 0 for bowling : "))
    if choose!=0 and choose!=1:
        print('Wrong choice match terminated')
    if choose==1:
        score1=0
        no=1
        while(True):
            print(no,end="")
            bat=int(input(" ball : "))
            bowl=rd.randint(0,6)
            if bat==bowl:
                print(user," are out")
                break
            if bat >=0 and bat <=6:
                score1+=bat
            print("Score : ",score1)
            no+=1
        print(user," have scored ",score1)
        no=1
        score2=0
        while(True):
            print(no,end="")
            bat=rd.randint(0,6)
            bowl=int(input(" ball : "))
            if bat==bowl:
                print("Computer is out")
                break
            if bowl >=0 and bowl <=6:
                score2 +=bat
            print("Score : ",score2)
            no+=1
            if score1<score2 :
                print("Computer have scored ",score2)
                print(user," have lost the match")
                mat=1
                break
        if score1>score2 and mat==0:
            print("Computer have scored ",score2)
            print(user," have won the match")
        if score1==score2 and mat==0:
            print("Computer have scored ",score2)
            print("The match is draw")
    if choose==0:
        score1=0
        no=1
        score2=0
        while(True):
            print(no,end="")
            bat=rd.randint(0,6)
            bowl=int(input(" ball : "))
            if bat==bowl:
                print("Computer is out")
                break
            if bowl >=0 and bowl <=6:
                score2+=bat
            print("Score : ",score2)
            no+=1
        print("Computer have scored ",score2)
        no=1
        while(True):
            print(no,end="")
            bat=int(input(" ball : "))
            bowl=rd.randint(0,6)
            if bat==bowl:
                print(user," is out")
                break
            if bat >=0 and bat <=6:
                score1+=bat
            print("Score : ",score1)
            no+=1
            if score1>score2:
                print(user," have scored ",score1)
                print(user," have won the match")
                mat=1
                break
        if score1<score2 and mat==0:
            print(user," have scored ",score1)
            print(user," have lost the match")
        if score1==score2 and mat==0:
            print(user," have scored ",score1)
            print("The match is draw")
else:
    print("Computer have won the toss")
    choose=rd.randint(0,100)
    choose=choose%2
    if choose==1:
        print("Computer is batting")
        score1=0
        no=1
        score2=0
        while(True):
            print(no,end="")
            bat=rd.randint(0,6)
            bowl=int(input(" ball : "))
            if bat==bowl:
                print("Computer is out")
                break
            if bowl >=0 and bowl <=6:
                score2+=bat
            print("Score : ",score2)
            no+=1
        print("Computer have scored ",score2)
        no=1
        while(True):
            print(no,end="")
            bat=int(input(" ball : "))
            bowl=rd.randint(0,6)
            if bat==bowl:
                print(user,"  out")
                break
            if bat >=0 and bat <=6:
                score1+=bat
            print("Score : ",score1)
            no+=1
            if score1>score2:
                print(user," have won the match")
                print(user," have scored ",score1)
                mat=1
                break
        if score1<score2 and mat==0:
            print(user," have scored ",score1)
            print(user," have lost the match")
        if score1==score2 and mat==0:
            print(user," have scored ",score1)
            print("The match is draw")
    if choose==0:
        print("Computer is bowling")
        score1=0
        no=1
        while(True):
            print(no,end="")
            bat=int(input(" ball : "))
            bowl=rd.randint(0,6)
            if bat==bowl:
                print("You are out")
                break
            if bat >=0 and bat <=6:
                score1+=bat
            print("Score : ",score1)
            no+=1
        print(user," have scored ",score1)
        no=1
        score2=0
        while(True):
            print(no,end="")
            bat=rd.randint(0,6)
            bowl=int(input(" ball : "))
            if bat==bowl:
                print("Computer is out")
                break
            if bowl >=0 and bowl <=6:
                score2+=bat
            print("Score : ",score2)
            no+=1
            if score1<score2:
                print("Computer have scored ",score2)
                print(user," have lost the match")
                mat=1
                break
        if score1>score2 and mat==0:
            print("Computer have scored ",score2)
            print(user," have won the match")
        else:
            print("Computer have scored ",score2)
            print("The match is draw")
