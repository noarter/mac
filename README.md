# mac
# 安装homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# 卸载homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)" 
sudo rm -rf /usr/local/

# 替换homebrew默认源
cd /usr/local
git remote set-url origin git://mirrors.ustc.edu.cn/brew.git

# 替换homebrew-core默认源
cd /usr/local/Library/Taps/homebrew/homebrew-core
git remote set-url origin git://mirrors.ustc.edu.cn/homebrew-core.git

# 替换homebrew bottles默认源
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bashrc
sourch ~/.bashrc

# maven镜像
https://repo.spring.io/libs-snapshot/
http://jcenter.bintray.com/
http://maven.springframework.org/release/
http://maven.aliyun.com/nexus/content/groups/public/

# github请求代理
git config --global http.proxy http://hx.gy:1080
# Android Studio
./android list sdk -u --proxy-host=hx.gy --proxy-port=1080
# composer镜像
{
    "repositories": [
        { "packagist": false },
        {
            "type": "composer",
            "url": "http://composer-proxy.jp/proxy/packagist"
        }
    ]
}
# npm
npm config set registry https://registry.npm.taobao.org 
# brew
cd /usr/local/ 
git remote set-url origin http://mirrors.ustc.edu.cn/homebrew.git 
brew update 

# jdk
cd  ~touch .bash_profile 
vi  .bash_profile 
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.7.0_45.jdk/Contents/Home 
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar 
export M2_HOME=/Library/apache-maven-3.3.9 
export PATH=$PATH:$JAVA_HOME/bin:$M2_HOME/bin  
source .bash_profile 
