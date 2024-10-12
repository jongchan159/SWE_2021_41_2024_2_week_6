# SWE_2021_41_2024_2_week_6

## Week 4 Assignment \
* Link of your repository
<pre>
<code>
def isHappy(n):
  #완료조건은 길이가 1일 때 까지
  #토큰값이 1이면 true
  #같은 값이 한번이라도 다시 나오면(무한루프) false

  sum = n # 새로운 n
  current = 0
  record = {sum} # 중복 검사를 위한 set

  while 1:
    digits = [int(digit) for digit in str(sum)] # 한자리수로 치환
    sum = 0
    for digit in digits:
      sum += digit*digit

    #제곱합이 1이면 true
    if sum == 1:
      return True
    #이미 존재하면 false
    if sum in record:
      return False
    #둘다 아니면 다시
    record.add(sum)

print(isHappy(19)) #True
print(isHappy(2)) #False
print(isHappy(7))
</code>

</pre>
* Description of your code
