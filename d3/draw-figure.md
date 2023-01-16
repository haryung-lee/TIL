## 도형 그리기

- svg 태그 안에서 circle, rect 등 다양한 도형을 제공한다.
- g태그는 그룹화를 하는 용도로 사용한다. 여러개의 그래프를 그릴 경우 여러개의 g태그를 사용해 위치를 조정한다. 위치를 조정할 때는 css의 transform을 사용한다.
- text 태그는 보통 legend, label, caption 등으로 사용한다. <br/>
  👉 일반 html 태그를 사용하지 않는다. 내부에서 작동하지만 x축과 y축으로 이동이 안된다.
- 셀렉팅이 되면 메서드 체이닝을 이용해 여러 속성들을 지정할 수 있다.
  ```javscript
  svg.append('text') // text 형태로 추가
    .attr('x', 200)
    .attr('y', 200)
    .attr('fill', 'black')
    .text('hello world')
    .style('font-weight', 'bold')
    .style('font-size', '34px')
    .style('font-family', 'Pacifico');
  ```
