# AWS Git 설정 가이드 (Ubuntu EC2)

## 1. Git 설치
\`\`\`bash
sudo dpkg --configure -a
sudo apt update -y
sudo apt install git -y
\`\`\`

## 2. 사용자 설정
\`\`\`bash
git config --global user.name "wisnoo-gif"
git config --global user.email "wisnoo0110@gmail.com"
\`\`\`

## 3. SSH 키
\`\`\`bash
ssh-keygen -t ed25519 -C "wisnoo0110@gmail.com"
cat ~/.ssh/id_ed25519.pub  # GitHub 등록
\`\`\`

## 4. 테스트 & 클론
\`\`\`bash
ssh -T git@github.com
git clone git@github.com:wisnoo-gif/my-study.git
cd my-study && mkdir aws-git
\`\`\`

