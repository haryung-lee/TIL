## Next13에서 svg사용 하기

[관련 이슈 참고](https://github.com/gregberge/svgr/issues/860)

## svg 색상 변경하기

svg 색상 바꾸려면 svg태그 안에 `fill: "currentColor"` `stroke: "currentColor"` 로 설정해주면 됨

## svg 크기 변경하기

svg 크기 바꾸려면 svg태그 안에 width=”current” height=”current”로 설정해주고

`<SvgIcon className="w-4 h-4" />` 이런식으로 바꿀 수 있음

## svg 안에 요소 짤림

기존 아이콘이 viewBox (0, 0, 24, 24) 였는데 일부 짤리는 현상이 있었음.
viewBox 설정에서 앞 두개가 minX, minY 인데 (시작 위치)이를 조정하면 됨.

하지만 실제 문제가 됐던 명확한 원인은 애초에 파일이 이상했음. 혹시 모르니 파일 자체에 문제가 있는지 확인할것. (다시 다운받기 등등..)

viewBox는 상대적인거기 때문에 어떤 값으로 하든 width, height이 증감하는 것에 영향 주지 x
하지만 viewBox가 viewPort(width, height)보다 작다면 잘릴 수 있음. 즉, viewBox를 잘 조절해야한다!

`viewPort`: 보여지는 영역. width, height으로 변경함.
`viewBox`: svg 내부 요소들의 좌표 영역과 비율, 그리고 뷰포트 내에서 도형을 보여줄 위치 설정

viewBox = “min-x min-y width height”
