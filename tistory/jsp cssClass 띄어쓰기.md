###jsp 컴파일된 class의 cssClass
회사에서 jsp java version을 1.7에서 1.8로 업그레이드 했다.  
그 때문인지는 모르겠지만 ..  
cssClass가 java tag로 들어간 부분에서!  
두개의 cssClass가 붙는 현상이 발생
컴파일된 class를 뜯어보니
out.print(" ")가 빠져있는걸 발견.

해결은 꼼수로 `" aClass "`로 해결하였고 정확한 원인을 찾지 못했다.
