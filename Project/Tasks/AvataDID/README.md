## 아바타에 DID를 적용하여 메타버스에 활용하기

### DID란
DID는 분산 신원을 나타내는 신원 관리 시스템의 약어이다. DID는 Decentralized Identifiers(분산 식별자)의 약어이며, 개인이나 조직의 디지털 신원을 식별하는 데 사용된다. DID는 중앙 집중식 서버가 아닌 분산된 네트워크에서 관리되며, 개인 데이터의 소유자가 데이터에 대한 통제를 유지할 수 있다. DID는 블록체인 기술을 활용하여 보안과 신원 확인을 강화할 수 있으며, 온라인 서비스 및 디지털 거래에서 더 높은 신뢰성과 개인 정보 보호를 제공할 수 있다.

### 메타버스에서 DID가 사용될 수 있는 상황
#
- 로그인 및 인증: 유니티 애플리케이션에서 사용자의 DID를 통해 로그인 및 인증을 처리할 수 있다. 사용자는 자신의 DID를 입력하고 해당 DID에 대한 인증 과정을 거친다. 이를 통해 중앙 집중식 로그인 시스템 대신 분산된 인증 메커니즘을 구현할 수 있다.

- 가상 자산 소유 및 거래: 유니티 메타버스 내에서 DID를 사용하여 아바타가 소유한 가상 자산을 관리하고 거래할 수 있다. 예를 들어, 유니티 애플리케이션에서 아바타가 소유한 가상 아이템을 DID와 연결하고, DID를 통해 소유권을 증명하고 거래를 수행할 수 있다.

- 개인 정보 보호 및 데이터 관리: 유니티 애플리케이션에서 DID를 활용하여 사용자의 개인 정보를 안전하게 관리할 수 있다. 사용자는 자신의 DID를 통해 개인 정보를 관리하고 필요에 따라 선택적으로 공유할 수 있다.

- 신원 확인 및 권한 관리: 유니티 메타버스에서 DID를 사용하여 사용자의 신원을 확인하고, 해당 신원에 기반한 권한 부여 및 접근 제어를 구현할 수 있다. 이를 통해 특정 기능이나 가상 공간에 대한 접근을 제한하거나 허용할 수 있다.

-> 로그인 및 인증 시스템 우선 구현 예정

### 유니티에서 DID를 사용하는 법
#
- DID 관리 라이브러리 선택: 먼저, DID를 관리하기 위한 라이브러리를 선택해야 한다. 여러 가지 오픈 소스 DID 라이브러리가 있으며, 예를 들어 uPort, Sovrin, 트루키(TruKey) 등이 있습니다. 선택한 라이브러리의 설치 및 설정 방법을 따른다.

- 유니티 프로젝트에 라이브러리 통합: 선택한 DID 라이브러리를 유니티 프로젝트에 통합해야 합니다. 이를 위해 해당 라이브러리의 Unity 플러그인이나 SDK를 가져오고, 프로젝트에 추가한다.

- DID 생성 및 관리: 라이브러리를 사용하여 유니티에서 DID를 생성하고 관리할 수 있습니다. 이는 사용자의 로그인, 인증 및 신원 확인을 처리하는 데 사용될 수 있습니다. 필요한 경우 사용자의 개인 정보, 키 쌍 등과 연결된 DID를 생성하고 관리한다.

- 신원 확인 및 인증: 유니티 애플리케이션에서 DID를 사용하여 사용자의 신원을 확인하고 인증할 수 있습니다. 사용자가 자신의 DID로 로그인하고, 해당 신원에 대한 인증 절차를 거친다.

- 자산 소유 및 거래: 유니티 메타버스 내에서 DID를 활용하여 사용자의 아바타가 소유한 가상 자산을 관리하고 거래할 수 있습니다. 이를 통해 아바타의 소유권을 증명하고, 가상 자산의 송수신 및 교환을 처리할 수 있다.

- 데이터 보호 및 개인 정보 관리: DID를 사용하여 유니티 애플리케이션 내의 사용자 데이터를 보호하고 개인 정보를 관리할 수 있습니다. 사용자는 자신의 DID와 연결된 데이터에 대한 접근과 공유를 관리할 수 있다.


### DID를 통해 로그인 기능 구현
#
- DID 라이브러리를 유니티 프로젝트에 통합
- 사용자 등록 및 DID 생성(회원가입) : 회원가입 UI 구현 후 사용자가 등록 정보를 입력하면 해당 정보를 기반으로 DID를 생성, 이때의 DID 생성 요청은 선택한 DID 라이브러리의 메서드를 사용하여 처리
- DID 인증 및 신원 확인(로그인) : 로그인 UI 구현 후 사용자가 입력한 ID와 비밀번호를 통해 로그인 요청을 처리한다. 이때 선택한 DID 라이브러리의 함수를 사용하여 DID를 통한 인증 및 신원 확인 절차를 진행한다.
- 로그인 성공 및 세션 관리: 인증 및 신원 확인이 완료되면 로그인이 성공한 것으로 간주한다. 이후 세션 관리를 위해 사용자의 로그인 상태를 유지하고, 필요한 경우 세션 토큰 또는 인증 토큰을 발급하여 애플리케이션에서 사용한다.
- 로그인 실패 및 오류 처리: 인증 및 신원 확인 과정에서 오류가 발생하거나 로그인이 실패한 경우에 대비한 오류 처리 기능을 구현한다. 이를 통해 사용자에게 적절한 오류 메시지를 표시하고 문제를 해결할 수 있는 안내를 제공한다.