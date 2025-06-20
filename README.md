# paiza_review

[paiza データ構造問題一覧](https://paiza.jp/works/mondai/data_structure/problem_index?language_uid=python3)

# 複数回のランダムアクセス 復習メモ

## 問題イメージ
- 要素数 N の数列 A と要素数 Q の数列 B が与えられる
- B の各要素 B_i 番目の A の値を Q 回出力する

### 入力例
5<br>
10 20 30 40 50<br>
3<br>
2 4 1<br>

## ポイント
- 入力形式が複数行なので、`N, Q = map(int, input().split())`はエラーになる
- 1行ずつ読み込んで、それぞれの変数に代入する

## コード例

```python
N = int(input())                 # 要素数Nを1行目で受け取る
A = list(map(int, input().split()))  # 数列Aを2行目で受け取る
Q = int(input())                 # 要素数Qを3行目で受け取る
B = list(map(int, input().split()))  # 数列Bを4行目で受け取る

for i in range(Q): #繰り返すrangeはQであって、Bではない。Bはリストだからエラーになる
    print(A[B[i] - 1])  # B_i番目の値を出力（1-index調整に-1を忘れずに）
```

## 別解

```python
N = int(input())                 # 要素数Nを1行目で受け取る
A = [int(x) for x in input().split()]  # 数列Aを2行目で受け取る
Q = int(input())                 # 要素数Qを3行目で受け取る
B = [int(y) for y in input().split()]  # 数列Bを4行目で受け取る

for i in range(Q):
    print(A[B[i]-1])
```

