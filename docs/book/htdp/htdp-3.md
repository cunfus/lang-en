# 程序就是函数加上变量定义

```scheme
;; profit : number -> number
;; 对于给定的 ticket-price，利润是收入和成本之差
(define (profit ticket-price)
  (- (revenue ticket-price) (cost ticket-price)))

;; revenue : number -> number
;; 对于给定的 ticket-price，计算收入
(define (revenue ticket-price)
  (* ticket-price (attendees ticket-price)))

;; cost : number -> number
;; 对于给定的 ticket-price，计算支出
(define (cost ticket-price)
  (+ 180 (* 0.4 (attendees ticket-price))))

;; attendees : number -> number
;; 对于给定的 ticket-price，计算观众数
(define (attendees ticket-price)
  (+ 120 (* 15 (/ (- 5 ticket-price) 0.1))))
```

对每种依赖关系，都使用一个辅助函数进行明确表达。

对于经常使用的变量数值，用一个常量表示它。如 `(define PI 3.1415926)`。



## 练习

### 3.1.1

```scheme
(attendees 5) ; 120
(attendees 4) ; 270
(attendees 3) ; 420
```

### 3.1.2

```scheme
(cost 5)    ; 228
(revenue 5) ; 600
(profit 5)  ; 372

(cost 4)    ; 288
(revenue 4) ; 1080
(profit 4)  ; 792

(cost 3)    ; 348
(revenue 3) ; 1260
(profit 3)  ; 912
```

价格 3 和 3.2 的利润是一致的，最优定价在 3.1 美元，利润 913.5 美元。

### 3.1.4

```scheme
(define (cost ticket-price)
  (* 1.5 (attendees ticket-price)))
```

修改 cost 后，定价在 3.6 和 3.7 美元收益最高，达到 693 美元。

### 3.3.1

```scheme
(define times_inch_to_cm 2.54)


(define (inches->cm inches)
  (* times_inch_to_cm inches))

(define (feet->inches feet)
  (* 12 feet))

(define (yards->feet yards)
  (* 3 yards))

(define (rods->yards rods)
  (* 5.5 rods))

(define (furlongs->rods furlongs)
  (* 40 furlongs))

(define (miles->furlongs miles)
  (* 8 miles))

(define (feet->cm feet)
  (inches->cm (feet->inches feet)))

(feet->cm 10)
```

### 3.3.2

```scheme

```