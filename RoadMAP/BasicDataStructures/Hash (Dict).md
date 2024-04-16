
1. Pocketmon

https://school.programmers.co.kr/learn/courses/30/lessons/1845

### My Solution()

- it is too long and hard to reading


``` python
def solution(nums):
    result = 0
    
    pocketmon_number = len(nums)
    maximum_pocketmon = pocketmon_number / 2
    pocketmon = {}
    
    for i in range(pocketmon_number):        
        if pocketmon.get(nums[i], False):
            continue
            
        pocketmon[nums[i]] = True        
        
        for j in range(i, pocketmon_number):
            if not pocketmon.get(nums[j], False): 
                pocketmon[nums[j]] = True
                
            if len(pocketmon) >= maximum_pocketmon:
                return len(pocketmon)
                
        if result < len(pocketmon):
           result = len(pocketmon)
                    
    return result
```


### Best Solution

- very simple and Intuitive


``` python
def solution(ls):
    return min(len(ls)/2, len(set(ls)))
```