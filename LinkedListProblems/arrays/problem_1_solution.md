matrix=[[1,2,3,4,5],[6,7,8,9,10],[11,12,13,14,15],[16,17,18,19,20],[21,22,23,24,25]]

def get_hr_glass_sum(matrix,row,col):
    sum = 0
    sum += matrix[row-1][col-1]
    sum += matrix[row-1][col]
    sum += matrix[row-1][col+1]
    sum += matrix[row][col]
    sum += matrix[row+1][col-1]
    sum += matrix[row+1][col]
    sum += matrix[row+1][col+1]
    return sum
    
max_hr_glass_sum = -63    
for i in range(1,4):
    for j in range(1,4):
        cur_hr_glass_sum = get_hr_glass_sum(matrix,i,j)
        if cur_hr_glass_sum > max_hr_glass_sum:
            max_hr_glass_sum = cur_hr_glass_sum
            
print(max_hr_glass_sum)