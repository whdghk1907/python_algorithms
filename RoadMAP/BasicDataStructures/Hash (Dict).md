https://school.programmers.co.kr/learn/courses/30/parts/12077
# 1. Pocketmon

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


# 2. Runner who didn't finish

### My Solution()

- too long and unintuitive 


``` python
def solution(participant, completion):
    runner_count = {}
    complet_count = {}
    
    for runner in participant:
        if runner in runner_count:
            runner_count[runner] += 1
        else:
            runner_count[runner] = 0
            
    for complet in completion:
        if complet in complet_count:
            complet_count[complet] += 1
        else:
            complet_count[complet] = 0
            
    for runner in runner_count:
        runner_num = runner_count[runner]
        if runner in complet_count:
            complet_num = complet_count[runner]
            if runner_num != complet_num:
                return runner
        else:
            return runner                

```