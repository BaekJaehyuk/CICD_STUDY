# GitHub Actions을 활용한 AWS Beanstalk CI/CD 파이프라인 구축


---

## CI (Continuous Integration)

-   코드 변경 사항을 공유 리포지토리에 푸시할 때마다 자동으로 통합 및 테스트되는 프로세스입니다. 

> GitHub Actions은 CI를 구현하는 데 사용되는 도구 중 하나로, GitHub 리포지토리의 이벤트에 따라 작업을 실행하고 테스트, 빌드 등의 작업을 수행할 수 있습니다. CI 도구에는 Jenkins, AWS CodePipeLine, Travis CI 등이 있습니다.
## CD (Continuous Deployment)

- CD는 CI 후에 성공적으로 통과된 코드 변경 사항을 자동으로 배포하는 프로세스입니다.

> AWS Elastic Beanstalk는 소프트웨어 애플리케이션을 자동으로 배포, 관리하는 서비스로, 코드를 업로드하면 Elastic Beanstalk가 배포 및 스케일링을 관리합니다.
---

## 설정
 ### 1. .github/workflows 디렉토리에 GitHub Actions 워크플로우 추가
   `.github/workflows` 디렉토리에 적절한 이름의 YAML 파일을 생성하여 GitHub Actions 워크플로우를 추가합니다. 이 워크플로우는 코드 변경 사항이 발생할 때마다 자동으로 실행됩니다.

 ### 2. AWS Beanstalk 환경 구성
   AWS Beanstalk에 애플리케이션 및 환경을 설정합니다. 환경 이름과 애플리케이션 이름은 GitHub Actions 워크플로우 파일에서 참조됩니다.

 ### 3. 코드 변경 및 푸시
   코드를 변경하고 GitHub 저장소에 푸시하면 GitHub Actions 워크플로우가 자동으로 실행됩니다. 워크플로우는 코드를 테스트하고 AWS Beanstalk에 배포합니다.


---

※ 테스트 : 2024-05-14
