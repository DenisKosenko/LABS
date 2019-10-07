- LAB3_2

- Варіант 7

    Визначити, чи існує прямокутний трикутник зі сторонами x, y, z, значення яких введено з клавіатури. Якщо так, обчислити його площу.

 <code>
 import math
    
    one = int(input())
    
    two = int(input())
    
    three = int(input())
    
    if (one + two) > three or (one + three) > two or (three + two) > one:
    
        per = (one + two + three)/2
        
        # print(per)
        
        s0 = per * (per - one) * (per - two) * (per - three)
    
        print(s0)
        
        if s0 < 0:
        
            s0 = s0 * -1
    
        s = math.sqrt(s0)
    
        print(s)
 </code>