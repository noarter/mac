# 安装homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# 卸载homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)" <br/>
sudo rm -rf /usr/local/

# 替换homebrew默认源
cd /usr/local <br/>
git remote set-url origin git://mirrors.ustc.edu.cn/homebrew.git

# 替换homebrew-core默认源
cd /usr/local/Library/Taps/homebrew/homebrew-core <br/>
git remote set-url origin git://mirrors.ustc.edu.cn/homebrew-core.git

# 替换homebrew bottles默认源
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bashrc <br/>
sourch ~/.bashrc

# maven镜像
https://repo.spring.io/libs-snapshot/ <br/>
http://jcenter.bintray.com/ <br/>
http://maven.springframework.org/release/ <br/>
http://maven.aliyun.com/nexus/content/groups/public/ <br/>

# github请求代理
git config --global http.proxy http://hx.gy:1080

# npm
npm config set registry https://registry.npm.taobao.org 

# jdk maven环境配置
cd  ~touch .bash_profile <br/>
vi  .bash_profile <br/>
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home <br/>
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar <br/>
export M2_HOME=/Library/apache-maven-3.3.9 <br/>
export PATH=$PATH:$JAVA_HOME/bin:$M2_HOME/bin  <br/>
source .bash_profile 
