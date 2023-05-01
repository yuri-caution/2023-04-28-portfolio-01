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

