# Tensorflow 常用指令

### 宣告

**常數**

`tf.constant()`

**變量**

`w = tf.Variable(tf.truncated_normal((fc7.get_shape()[-1].value, nb_classes), stddev=1e-2))`

`b = tf.Variable(tf.zeros(nb_classes))`

**亂數**

`tf.truncated_normal(size, mean, stddev)`

`tf.random_normal(size, mean, stddev)`



---

### Math

**加、減、乘、除**

`x = tf.add(5, 2) `
`x = tf.subtract(10, 4)`
`x = tf.multiply(2, 5)`
`x = tf.device(10)`

**x * w + b**

`tf.nn.xw_plus_b(x, w, b)`

**Softmax**

`tf.nn.softmax(x)`

`tf.nn.softmax_cross_entropy_with_logits_v2(labels=one_hot_y, logits=logits)`

`tf.nn.sparse_softmax_cross_entropy_with_logits(logits, labels)`

**平均**

`tf.reduce_mean()`



------

### 前處理

**輸入**

`x = tf.placeholder(tf.float32, [None, 28, 28, 1])`

**轉成one hot**

`one_hot_y = tf.one_hot(y, nb_classes)`

**Resize**

`resize = tf.image.resize_images(x, (227, 227))`

**分類 Train and test data**

`X_train, X_valid, y_train, y_valid = train_test_split(data['features'], data['labels'], test_size=0.33, random_state=0)`



---

# Udacity_Notebook
