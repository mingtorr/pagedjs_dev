# Discovered Issues

## when page-break
1. 페이지의 나머지 공간보다 이미지의 높이가 크면 다음 페이지로 넘어가지 않고 이미지가 잘림
2. 테이블에 rowspan이 여러 개면 다음 페이지의 테이블이 깨짐 (첫 rowspan은 제대로 그리지만 두번째 이후 rowspan 부터 제대로 출력되지 않음)
- rebuildTableRow 가 이전 row를 기준으로 rowspan 계산을 해서 중첩된 rowspan 계산이 정상적으로 이루어지지 않음
3. thead가 여러 row이고 colspan 이 적용되어 있으면 colspan의 출력이 깨짐
4. 상위 div의 margin 계산이 누락되어 정상적으로 잘리지 않음
5. td 안에 이미지가 있으면 페이지 분할이 제대로 이루어지지 않음
6. td가 2줄 이상일 때 정상적으로 잘리지 않음
7. 테이블이 열 분할시 thead 를 다시 그리지 않아 td 크기가 틀어짐
8. padding-top: unset; 에 의해 td 안의 padding-top 까지 사라짐

## other
1. page size 가 letter로 설정되어 있어 Ctrl + p 출력 시 여백 발생 (한국 기본 출력은 A4)
