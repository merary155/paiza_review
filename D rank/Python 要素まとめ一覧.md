### .sort() 
##### 数字だけ、または文字列だけのリストに使う

nums = [4, 2, 9, 1]<br>
nums.sort()<br>
print(nums)  # [1, 2, 4, 9]<br>

words = ['banana', 'apple', 'cherry']<br>
words.sort()<br>
print(words)  # ['apple', 'banana', 'cherry']<br>

##### 数字と文字列が混ざるとエラーになる
##### mixed = [3, 'apple', 5]
##### mixed.sort()  # TypeErrorになる

##### 降順の時は"reverse=True"を()に入れるだけ
