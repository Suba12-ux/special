def quad(x):
    txt = []
    q = 1
    while q:
        if x<1:
            break
        if x%2!=0:
            txt += '1'
            x = x//2
            continue
        else:
            txt += '0'
            x = x//2
            continue
    txt.reverse()
    t = txt.pop(0)
    txt.extend(t)
    return txt
def teng(x):
    q = len(x)-1
    w = 0
    for i in range(len(x)):
        w += int(x[i])*(2**q)
        q -= 1
        #print(w)
        #print(q, end='') 
    return w
    
x1, x2 = int(input()), int(input())    

print(teng(quad(x1)))