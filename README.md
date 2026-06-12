# HSI_AD
Submodule은 "내 Git 저장소 안에 다른 Git 저장소를 포함시키는 기능" 입니다.
연구할 때 여러 논문 코드를 한 곳에서 관리하기에 좋습니다.
겉으로는 폴더처럼 보이지만 실제로는 각각 독립적인 Git Repository입니다.

1. 상위 저장소 생성
먼저 GitHub에 빈 저장소를 하나 만듭니다.
로컬로 가져오기 (git clone https://github.com/username/HSI-AD.git)

2. Submodule 추가
git submodule add https://github.com/amazon-science/patchcore-inspection.git PatchCore

3. 상위 저장소 Commit
git add .
git commit -m "Add submodules"
git push

4. 다른 PC에서 Clone
일반 Clone 하면 Submodule 내부가 비어있을 수 있습니다.
따라서
git clone --recursive https://github.com/username/HSI-Research.git
사용하는 것이 좋습니다.
또는
git submodule update --init --recursive
