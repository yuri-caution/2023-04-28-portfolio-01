##포트폴리오 페이지 레이아웃

### :before 사용
```
.hero .photo {
    /* flex: 1; */
    width: 500px;
    position: relative;
}

.hero .photo img {
    display: block;
    border-radius: 100%;
    border-top-right-radius: 0;
}

.hero .photo::before {
    content: '';
    position: absolute;
    top: -20px;
    left: -20px;
    width: 500px;
    height: 500px;
    background-color: #b2ffff;
    z-index: -1;
    border-radius: 100%;
    border-top-right-radius: 0;
}
```

### grid 사용
```
.works ul {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 45px;
}

.works ul li .photo {
    height: 330px;
}

.works ul li .photo img {
    height: 100%;
    object-fit: cover;
}
```

### max-width
```
/* container */

.container {
    max-width: 1100px;
    padding: 0 10px;
    margin: 0 auto;
}
```

### script 작성
##### 변수 이름 변경될 수 있으므로 this로 작성하기도
```
<script>
        const btn = document.querySelector('.bars i')
        const gnb = document.querySelector('.gnb')

        btn.addEventListener('click', function(){
            gnb.classList.toggle('active')
            this.classList.toggle('xi-close')
        })

        // console.log(btn)
        // console.log(gnb)
</script>
```

### hover 효과 넣기
#### 마크업에 span 으로 글자 영역 묶기
```
<ul class="gnb">
    <li><a href="#"><span>소개</span></a></li>
    <li><a href="#"><span>작업</span></a></li>
    <li><a href="#"><span>연락하기</span> </a></li>
</ul>
```

#### css 작성
```
.gnb li a:hover {
    color: tomato;
}

.gnb li a span {
    display: block;
    position: relative;
}

.gnb li a span::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: tomato;
    width: 0;
    height: 3px;
    transition: all 0.3s;
}

.gnb li a:hover span::after {
    width: 100%;
}
```
