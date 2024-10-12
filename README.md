# SWE_2021_41_2024_2_week_6

## Week 4 Assignment 
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
* Description of your code \
코드에 설명되어있듯이 \
  * 성공 조건은 sum값이 1이 나왔을 때
  * 실패 조건은 같은 값이 중복으로 나왔을 때(무한루프)
line 16~20: 숫자 sum을 문자열로 변환해서 숫자 하나씩 토큰화, 토큰화한 문자열 형태의 숫자를 다시 정수 형태로 digits 리스트에 삽입함. 이후 각 정수를 곱하는 연산을 하고, 다시 sum의 값으로 대입함.
line 22~29: 연산한 sum의 결과에 따라 1이면 True, 중복이면 False, 둘 다 아니면 루프를 다시 실행
line 31~33: 결과를 출력
