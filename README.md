# etc-passwd
What is path etc/password -IGLOO Corporation Won Chi Hyun-

특히 /etc 디렉터리는 환경설정에 관련된 파일을 가지고 있습니다.

환경설정에 관련된 파일은 사용자 패스워드 정보를 가지고 있는 passwd 파일 passwd 파일의 인증 방식은 해시값 인증방식이다.
만약 공격자가 /etc 파일 경로로 접근하여 사용자 패스워드 정보를 가지고 있는 passwd 파일 혹은  shadow 파일과 프로토콜 및 서비스 정보를 보유한 protocol, servies 파일 등에 접근을 시도한다면
미리 앞단에서 차단해야할 필요성이 있습니다.

/etc/passwd 파일에는 해시로 암호화된 패스워드가 있지만, /etc/passwd에 패스워드를 저장하지 않고 /etc/shadow 파일에 패스워드를 저장할 수 있습니다.

/etc/passwd 은 시스템에 로그인하는 사용자 계정을 관리하는 text 파일로
root 계정 뿐만 아니라 다른 계정에게도 읽기 권한이 있어 누구나 읽을 수 있지만, 수정은 root 만 가능

file inclusion 과 같이 상위 경로로 이동하면서 etc/passwd 파일에 접근하면 사용자의 계정 정보를 탈취할 수 있는 위험이 있으므로 접근 차단해야함.
