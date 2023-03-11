# data_structure_2

# Knapsack Algorithm method   
  
   
weight = [30,50,10,70,40]
value = [150,100, 90, 140, 120]
capacity = 150 

def fractional_knapsack(value, weight, capacity):
    items = list(range(len(value)))
    print(1,items)
    ratio = [v// w for v, w in zip(value, weight)]
    print(2,ratio)
    
    str_ratios = sorted(ratio, reverse= True)
    print(3, str_ratios)
    items.sort(key=lambda i: ratio[i], reverse=True)
    
    max_value = 0 
    fractions = [0]* len(value)
    print(4,fractions)    
    for i in items:
        if weight[i] <= capacity:
            fractions[i] = 1 
            max_value += value[i]
            capacity -= weight[i]
            
        else:
            fractions[i] = capacity // weight[i] 
            
    return max_value 

print(fractional_knapsack(value, weight, capacity))


END>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>..........END..............>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>END





