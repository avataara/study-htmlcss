# 10 CSS3 ��ȯ
HTML5���� 3������ �����ϴ� ���
- �ڹٽ�ũ��Ʈ�� ����� WebGL : WebGL�� �� ����� �׷��� ���̺귯���̴�. �ڹٽ�ũ��Ʈ ���α׷��� �� ���ؼ� ����� �� ������ ȣȯ���� �ִ� �� ���������� ���ͷ�Ƽ���� 3D �׷����� ����� �� �ֵ��� �����ȴ�.
- CSS3�� ����� 3���� ��ȯ

## 10.1 2���� ��ȯ
X,Y���� �ִ� ȭ�� ��ǥ
### 10.1.1 transform �Ӽ�
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <style>
        section {
            width: 100px; height: 100px;
            border: 5px solid black;
        }
        div {
            width: 100px;
            height: 100px;
            background: red;
            -ms-transform: rotate(60deg);
            -moz-transform: rotate(60deg);
            -o-transform: rotate(60deg);
            -webkit-transform: rotate(60deg);
            transform: rotate(60deg);
        }
    </style>
</head>
<body>
    <section>
        <div></div>
    </section>
</body>
</html>
```
### 10.1.2 2���� ��ȯ �Լ�
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <style>
        section {
            width: 100px; height: 100px;
            border: 5px solid black;
        }
        div {
            width: 100px; height: 100px;
            background: red;
            -ms-transform: rotate(60deg) scale(1.2) skewY(10deg);
            -moz-transform: rotate(60deg) scale(1.2) skewY(10deg);
            -o-transform: rotate(60deg) scale(1.2) skewY(10deg);
            -webkit-transform: rotate(60deg) scale(1.2) skewY(10deg);
            transform: rotate(60deg) scale(1.2) skewY(10deg);
        }
    </style>
</head>
<body>
    <section>
        <div></div>
    </section>
</body>
</html>
```
*��ȯ �Լ� ���� �߿�*
### 10.1.3 transform-origin �Ӽ�
�⺻�� �±׿����� �߽��� ��ȯ �߽����� ��´�.
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <style>
        section {
            width: 100px; height: 100px;
            border: 5px solid black;
        }
        div {
            width: 100px;
            height: 100px;
            background: red;
            -ms-transform: rotate(60deg);
            -moz-transform: rotate(60deg);
            -o-transform: rotate(60deg);
            -webkit-transform: rotate(60deg);
            transform: rotate(60deg);

            -ms-transform-origin: 100% 100%;
            -moz-transform-origin: 100% 100%;
            -o-transform-origin: 100% 100%;
            -webkit-transform-origin: 100% 100%;
            transform-origin: 100% 100%;
        }
    </style>
</head>
<body>
    <section>
        <div></div>
    </section>
</body>
</html>
```
## 10.2 3���� ��ȯ
### 10.2.1 3���� ��ȯ �Լ�
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <style>
        body {
            width: 200px;
            margin:200px auto;
        }
        section{width: 200px;height: 200px; position: relative}
        div {
            width: 200px;
            height: 200px;
            position:absolute; left:0; top:0;
            opacity:0.3;
        }
        /* ���� */
        div:nth-child(1) {transform: rotateY(0deg) translate3d(0,0,100px);background-color: red;}
        div:nth-child(2) {transform: rotateY(90deg) translate3d(0,0,100px);background-color: green;}
        div:nth-child(3) {transform: rotateY(180deg) translate3d(0,0,100px);background-color: blue;}
        div:nth-child(4) {transform: rotateY(270deg) translate3d(0,0,100px);background-color: yellow;}
        /* ����� �Ʒ��� */
        div:nth-child(5) {transform: rotateX(90deg) translate3d(0,0,100px);background-color: brown;}
        div:nth-child(6) {transform: rotateX(270deg) translate3d(0,0,100px);background-color: pink;}
    </style>
</head>
<body>
    <section>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>
</body>
</html>
```
### 10.2.1 transform-style �Ӽ�
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <style>
        body {
            width: 200px;
            margin:200px auto;
        }
        section{
          width: 200px;height: 200px;
          position: relative;
          animation: rint 3s linear 0s infinite;
          /*transform-style: preserve-3d;*/
        }
        @keyframes rint {
          from {
            transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg);
          }
          to {
            transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg);
          }
        }
        div {
            width: 200px;
            height: 200px;
            position:absolute; left:0; top:0;
            opacity:0.3;
        }
        /* ���� */
        div:nth-child(1) {transform: rotateY(0deg) translate3d(0,0,100px);background-color: red;}
        div:nth-child(2) {transform: rotateY(90deg) translate3d(0,0,100px);background-color: green;}
        div:nth-child(3) {transform: rotateY(180deg) translate3d(0,0,100px);background-color: blue;}
        div:nth-child(4) {transform: rotateY(270deg) translate3d(0,0,100px);background-color: yellow;}
        /* ����� �Ʒ��� */
        div:nth-child(5) {transform: rotateX(90deg) translate3d(0,0,100px);background-color: brown;}
        div:nth-child(6) {transform: rotateX(270deg) translate3d(0,0,100px);background-color: pink;}
    </style>
</head>
<body>
    <section>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>
</body>
</html>
```
### 10.2.1 backface-visibility �Ӽ�
backface-visibility �Ӽ��� 3���� �������� ����� �ĸ��� ���̰ų� ���ų� �Ӽ�
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <style>
        body {
            width: 200px;
            margin:200px auto;
        }
        section{
          width: 200px;height: 200px;
          position: relative;
          animation: rint 3s linear 0s infinite;
          transform-style: preserve-3d;
        }
        @keyframes rint {
          from {
            transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg);
          }
          to {
            transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg);
          }
        }
        div {
            width: 200px;
            height: 200px;
            position:absolute; left:0; top:0;
            opacity:0.3;
            /* backface-visibility: hidden; */
        }
        /* ���� */
        div:nth-child(1) {transform: rotateY(0deg) translate3d(0,0,100px);background-color: red;}
        div:nth-child(2) {transform: rotateY(90deg) translate3d(0,0,100px);background-color: green;}
        div:nth-child(3) {transform: rotateY(180deg) translate3d(0,0,100px);background-color: blue;}
        div:nth-child(4) {transform: rotateY(270deg) translate3d(0,0,100px);background-color: yellow;}
        /* ����� �Ʒ��� */
        div:nth-child(5) {transform: rotateX(90deg) translate3d(0,0,100px);background-color: brown;}
        div:nth-child(6) {transform: rotateX(270deg) translate3d(0,0,100px);background-color: pink;}
    </style>
</head>
<body>
    <section>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>
</body>
</html>

```
## 10.3 ���ٹ�
ȭ�鿡 �󸶳� ���� 3���� �ȼ��� ���� ������ ����
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS3 Transform Basic</title>
    <script src="prefixfree.min.js"></script>
    <style>
        body {
            width: 200px;
            margin:200px auto;
            perspective:400px;
        }
        section{
          width: 200px;height: 200px;
          position: relative;
          animation: rint 3s linear 0s infinite;
          transform-style: preserve-3d;
        }
        @keyframes rint {
          from {
            transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg);
          }
          to {
            transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg);
          }
        }
        div {
            width: 200px;
            height: 200px;
            position:absolute; left:0; top:0;
            opacity:0.3;
            /* backface-visibility: hidden; */
        }
        /* ���� */
        div:nth-child(1) {transform: rotateY(0deg) translate3d(0,0,100px);background-color: red;}
        div:nth-child(2) {transform: rotateY(90deg) translate3d(0,0,100px);background-color: green;}
        div:nth-child(3) {transform: rotateY(180deg) translate3d(0,0,100px);background-color: blue;}
        div:nth-child(4) {transform: rotateY(270deg) translate3d(0,0,100px);background-color: yellow;}
        /* ����� �Ʒ��� */
        div:nth-child(5) {transform: rotateX(90deg) translate3d(0,0,100px);background-color: brown;}
        div:nth-child(6) {transform: rotateX(270deg) translate3d(0,0,100px);background-color: pink;}
    </style>
</head>
<body>
    <section>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>
</body>
</html>

```
## 10.4 ȸ����
### 10.4.1 body �±� ����
### 10.4.2 ��Ÿ�� ���
### 10.4.3 �ִϸ��̼� ����
