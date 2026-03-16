sudo dpkg --configure -a
sudo apt update -y
sudo apt install git -y

git config --global user.name "wisnoo-gif"
git config --global user.email "wisnoo0110@gmail.com"

ssh-keygen -t ed25519 -C "wisnoo0110@gmail.com"  # Enter 3번
cat ~/.ssh/id_ed25519.pub  # 복사 > GitHub SSH key 등록

테스트: ssh -T git@github.com  # Hi wisnoo-gif!

Repo: https://github.com/wisnoo-gif/my-study.git

클론: git clone git@github.com:wisnoo-gif/my-study.git
cd my-study

폴더 추가:
mkdir aws-practice
echo "# AWS에 git연동하기" > aws-git/README.md
git add .
git commit -m "AWS Git 설정"
git push origin main
