# 결론

모든 것이 예상대로 진행 되었다면 이전과 동일한 프론트 엔드에서 실행 가능한 실제 운영 환경을 사용할 수 있습니다. Beanstalk이 환경 대시 보드에서 제공하는 것을 탐색 할 시간을 가지십시오. 흥미로운 통계 및 건강 상태 보고서가 많이 있습니다.

Beanstalk의 더 가치있는 기능은 동일한 응용 프로그램의 환경을 독립적으로 설정하고 종료 할 수있는 기능입니다. 이것은 실제 프로젝트에서 작업 할 때 큰 변화를 일으 킵니다. 변경 사항을 프로덕션으로 이동하기 전에 테스트해야하고, 새로운 사람들이 진행중인 프로젝에 합류하거나 떠납니다. 그와중에 개발중인 애플리케이션을 팀원이 고장내지않게 하면서 데모를 해야합니다.  이런상황이 바로 Elastic Beanstalk 이 빛을 발휘하는 때입니다.

---
**도전 과제:**

- 최신 앱 아키텍처 (S3의 프론트 엔드 및 EC2의 API)에 대해 생각해 보면 다중 환경 시나리오를 최대한 활용하는 데 이상적인 조합은 아닙니다. 이 작업을 수행하는 방법에는 여러 가지 옵션이 있으며 사례에 따라 모두 좋고 나쁨이 있습니다. 이것을 생각해보고 환경 관리를보다 단순하게 만들고 구현할 수있는 방법에 대해 생각해보십시오.

Beanstalk 사용에 앞서 가장 큰 걸림돌은?

- [앞서](/workshop/beanstalk/introduction.md) 말했듯이 Beanstalk 안에 프로덕션 RDS를 관리하는것 은 추천하지 **않습니다**. 이유는 환경구성을 위해서 Beanstalk은 인스턴스를 상태 비저장으로 다뤄야만 합니다만, 데이타베이스는 그 반대입니다.

**Conduit-staging** 이라는 내부 RDS가있는 새로운 환경을 만들어보십시오.
