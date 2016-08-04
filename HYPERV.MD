##Docker 학습 공간##
- - -
윈도우에서 도거를 학습 하기 위한 공간입니디.</br>
Windows 10 Pro에서 Docker를 실행 하기전에 Windows의 Hyper-v에 대해서 살펴 본다

Hyper-V는 실제 호스트를 기반으로 실행 중인 가상화된 컴퓨터 시스템을 활성화합니다. 이러한 가상화된 시스템을 물리적 컴퓨터 시스템인 것처럼 사용 및 관리할 수 있지만 가상화된 격리된 환경에 존재합니다. 하이퍼바이저라는 특별한 소프트웨어는 가상 시스템과 실제 하드웨어 리소스 간의 액세스를 관리합니다. 가상화를 통해 컴퓨터 시스템, 이전에 알려진 양호한 상태로 신속하게 시스템을 복원하는 방법 및 물리적 호스트 간에 마이그레이션하는 기능을 빠르게 배포할 수 있습니다.

1. Hyper-V을 설치 합니다. 

    Windows 10에서 가상 컴퓨터를 만들려면 먼저 Hyper-V 역할을 활성화해야 합니다. Windows 10 제어판, PowerShell 또는 배포 이미지 서비스 및 관리 도구(DISM)를 사용하여 실행할 수 있습니다. 이 문서는 이러한 단계를 살펴 봅니다.
    
    [참고 :: Windows 10에 Hyper-V 설치](https://msdn.microsoft.com/ko-kr/virtualization/hyperv_on_windows/quick_start/walkthrough_install)

2. 가상 스위치 만들기

    Hyper-V에서 가상 컴퓨터를 만들려면 먼저 이 가상 컴퓨터를 실제 네트워크에 연결하는 방법을 제공해야 할 수 있습니다. Hyper-V는 가상 컴퓨터의 네트워크 카드를 가상 스위치에 연결할 수 있는 소프트웨어 기반 네트워킹 기술을 포함하여 네트워크 연결을 제공합니다. Hyper-V에서 만든 각 가상 스위치는 세 가지 연결 유형 중 하나로 구성할 수 있습니다.

    * 외부 네트워크 – 가상 스위치는 실제 네트워크, Hyper-V 호스트 및 가상 컴퓨터 간의 연결을 제공하는 실제 네트워크 어댑터에 연결됩니다. 이 구성에서는 물리적으로 연결된 네트워크 카드를 통해 통신할 수 있는 호스트의 기능을 사용하거나 사용하지 않도록 설정할 수도 있습니다. 이는 특정 실제 네트워크 카드에 VM 트래픽만을 격리하는 데 유용할 수 있습니다.

    * 내부 네트워크 – 가상 스위치가 실제 네트워크 어댑터에 연결되어 있지 않습니다. 그러나 Hyper-V 호스트와 이 스위치에 연결된 모든 가상 컴퓨터 간에는 네트워크 연결이 있습니다.

    * 개인 네트워크 – 가상 스위치가 실제 네트워크 어댑터에 연결되어 있지 않고 Hyper-V 호스트와 이 스위치에 연결된 가상 컴퓨터 간에 연결이 없습니다.

    [참고 :: 가상 스위치 만들기](https://msdn.microsoft.com/ko-kr/virtualization/hyperv_on_windows/quick_start/walkthrough_virtual_switch)

3. Hyper-V 관리자를 사용하여 가상 컴퓨터 만들기

    가상 컴퓨터를 만들고 Windows 배포 서비스를 사용하거나 준비된 가상 하드 드라이브를 연결하거나 수동으로 설치 미디어를 사용하는 등 다양한 방법으로 운영 체제를 배포할 수 있습니다.

    [참고 :: Hyper-V 관리자를 사용하여 가상 컴퓨터 만들기](https://msdn.microsoft.com/ko-kr/virtualization/hyperv_on_windows/quick_start/walkthrough_create_vm)

4. Hyper-V 및 Windows PowerShell 사용

    Hyper-V 배포, 가상 컴퓨터 만들기 및 이러한 가상 컴퓨터 관리의 기본 사항을 살펴보았으므로 이제 PowerShell 사용하여 이러한 다양한 작업을 자동화할 수 있는 방법을 살펴보겠습니다

    [참고 :: Hyper-V 및 Windows PowerShell 사용](https://msdn.microsoft.com/ko-kr/virtualization/hyperv_on_windows/quick_start/walkthrough_powershell)
