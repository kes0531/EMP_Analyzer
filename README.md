# EMP_Analyzer
케이쉴드 주니어 

보안사고 분석대응 7기 팀프로젝트 (21.08.~21.11.)

## Entered Malicious Packet Analyzer (EMP_Analyzer)
#### 악성 패킷을 자동으로 분석해주고 결과를 보기 쉬운 리포트 형태로 표시해주는 도구

1. 악성이 의심되는 패킷(pcap, pcapng)을 입력
2. 패킷을 모두 읽고 TCP위주로 패킷을 분류
3. 미리 작성된 YARA Rule을 통해 패턴 매칭
4. 매칭된 페이로드가 파일이라면 추출 후 실제 악성 여부 판단을 위해 바이러스토탈 API를 통해 검색
5. 매칭된 패킷의 IP를 기반으로 별도 pcap 추출
6. 웹 브라우저를 통한 리포트 출력
#### 담당 파트
YARA Rule에 매칭된 TCP 스트림 분류 모듈, 바이러스토탈 API 검색 모듈<br>
웹 리포트 작성 자동화 & 리포트 탬플릿 작성 모듈

시연 영상 : https://youtu.be/yT4vRVQmgik