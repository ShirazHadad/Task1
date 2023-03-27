# Task1
### Task1 Data mining and analysis

### Q1
def My_func(x1,x2,x3):
  try:
        counter = (x1+x2+x3)*(x2+x3)*x3
        denominator = x1+x2+x3
        #if not (isinstance(x1, float)) and not (isinstance(x2, float)) and not (isinstance(x3, float)):
        if type(x1) is int or type(x2) is int or type(x3) is int:
            print("Error: parameters should be a float")
            #return None #when the value is wrong type, like int or str...
        elif denominator == 0:
            print("Not a number - determinator equals zero")
        else:
            result = counter/denominator
            return result
    except:
        if type(x1) is not float or type(x2) is not float or type(x3) is not float:
            print("None")
#My_func(2.0,5.2,6.2)
#My_func(-3.0,5.0,-2.0)
#My_func("six",5.0,2.0)
#My_func("one","two","three")
#My_func(1.8,6,3.0)
#My_func(18,6,500)

## Q2

def revword(word:str):
    word = word[::-1]
    word = word.lower()
    return word

def countword():
    file = open('text.txt', 'r')
    lst = list()
    count = 1
    for line in file:
        lines = line.rstrip().split()
        if len(lst) == 0:
            word = lines[0]
            lst.append(lines)
            #print(lst)
        else:
            for singleword in lines:
                reverse = revword(singleword)
                #print(reverse)
                if reverse == word:
                    count = count+1
                    
print("The number of times the first word in the text appears is:", count)
    
countword()
