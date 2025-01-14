## **🔎 JAVA 언어의 장단점**

---

### **✔️ 장점**

1️⃣ 자바 언어는 이식성이 높은 언어이기 때문에 자바 언어로 개발된 프로그램은 소스 파일을 수정하지 않더라도, 자바 실행 환경(JRE)이 설치되어 있는 모든 운영체제에서 실행이 가능하다.

2️⃣ 자바 언어는 객체 지향 프로그래밍으로 개발하는 기법을 이용하며 부품에 해당하는 객체들을 먼저 만들어 두고 조립하여 전체 프로그램을 만든다. 또한 자바 언어는 100% 객체 지향 언어이며, 설계도에 해당하는 클래스를 작성하고 객체와 객체를 연결하여 목적에 맞는 프로그램을 만든다. 또한 캡슐화, 상속, 다형성 기능을 완벽하게 지원한다.

3️⃣ 자바 언어는 함수적 프로그래밍을 지원하여 대용량의 데이터 병렬 처리와 이벤트 지향 프로그래밍이 적합하여 최근 다시 주목받고 있다. 자바 8부터 함수적 프로그래밍을 지원하는 람다식을 사용하여 컬렉션 요소를 필터링, 매핑, 집계 처리하는 게 간단해졌고, 코드가 매우 간결해졌다.

4️⃣ 자바 언어는 개발자가 직접 메모리에 접근할 수 없고 자바가 직접 메모리를 관리한다. 객체를 생성할 때 자동으로 메모리 영역을 찾아 할당하고, 사용이 완료되면 Garbage Collector를 실행하여 자동적으로 사용하지 않는 객체를 제거한다. 덕분에 메모리 관리의 수고가 줄고, 코드 구현에 집중할 수 있다.

5️⃣ 자바 언어는 윈도우, 리눅스, 유닉스, 맥 등 여러 OS에서 실행되는 프로그램을 개발할 수 있다. 그리고 콘솔 프로그램, 클라이언트용 윈도우 애플리케이션, 서버용 웹 애플리케이션, 모바일용 안드로이드앱 등 거의 모든 곳에서 실행되는 프로그램을 개발할 수 있다.

6️⃣ 자바 언어는 Dynamic Loading, 동적 로딩을 지원하는데, 애플리케이션이 실행될 때 모든 객체가 생성되는 것이 아닌, 각 객체가 필요한 시점에 클래스를 동적 로딩해서 생성한다. 그리고 유지보수 시에 해당 클래스만 수정하면 되기 때문에 전체 애플리케이션을 다시 컴파일할 필요가 없기 때문에 유지보수가 용이하고 빠르다.

7️⃣ 자바 언어는 오픈소스 언이이기 때문에 자바 프로그램에서 사용하는 라이브러리 또한 오픈소스가 많은 편이다. 오픈소스 라이브러리를 통해 개발 시간을 단축하고 안정성이 높은 애플리케이션을 개발하기 용이하다.

---

### **✔️ 단점**

1️⃣ 자바 언어는 JVM 로딩 속도 문제, 가상 머신 바이트코드 실행 속도 문제, 가비지 컬렉션에 의한 실행 지연 문제 등이 존재한다. JVM 로딩 속도 문제는 플랫폼에 상관없이 바로 자바를 실행하는 것에 도움이 되지만 환경이 모두 로딩되어야 실행되는 단점이 있다. 

가상 머신 바이트코드 실행 속도 문제는 JIM의 탄생 기점으로 이전에 비해서는 속도가 많이 개선 됐지만 메모리 용량 뒷받침이 필수적이고 Java9 이후 버전부터만 조금 더 적극적으로 속도를 극복할 수 있다. 

가비지 컬렉션에 의한 실행지연 문제는 실시간 응용 시스템에 부적합한 내용과 동일한 문제점으로 본다. 메모리를 자동으로 변환하는 것 때문에 자동화된 메모리 변환이 언제 메모리를 확인하고 프로그램에 있는 자료들을 확인할지 모르기 때문이다.

2️⃣ 자바 언어는 다른 언어들과 달리 프로그램 실행 시에 발생할 수 있는 예외들을 개발자가 직접 선언하여 처리해야 한다. 그렇지 않으면 아예 컴파일이 되지 않는다. (try - catch 등을 활용하는데 높은 안정성을 위해 상황에 맞는 예외 처리를 반드시 사용한다.)
