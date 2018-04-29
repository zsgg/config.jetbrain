#####[The performance benefits of rel=noopener](https://jakearchibald.com/2016/performance-benefits-of-rel-noopener/)
####[Tabnabbing 공격과 rel=noopener 속성](https://blog.coderifleman.com/2017/05/30/tabnabbing_attack_and_noopener/)
Tabnabbing이란 HTML 문서 내에서 링크(target이 _blank인 Anchor 태그)를 클릭 했을 때 새롭게 열린 탭(또는 페이지)에서 기존의 문서의 location을 피싱 사이트로 변경해 정보를 탈취하는 공격 기술을 뜻한다. 이 공격은 메일이나 오픈 커뮤니티에서 쉽게 사용될 수 있다.

noopener 속성을 사용해 열린 탭은 부모를 호출할 일이 없다. 따라서 같은 스레드 일 필요 없으며 새로운 페이지가 느리다고 부모 탭까지 느려질 일도 없다.