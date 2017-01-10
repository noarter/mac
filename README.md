# mac
mac安装homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

#maven镜像
http://uk.maven.org/maven2/
https://repo.spring.io/libs-snapshot/
http://maven.wso2.org/nexus/content/groups/public/
http://jcenter.bintray.com/
http://maven.antelink.com/content/repositories/central/
http://nexus.openkoala.org/nexus/content/groups/Koala-release/
http://maven.tmatesoft.com/content/groups/public/
http://mavensync.zkoss.org/maven2/
http://maven.springframework.org/release/
http://maven.aliyun.com/nexus/content/groups/public/

#github请求代理
git config --global http.proxy http://hx.gy:1080
#Android Studio
./android list sdk -u --proxy-host=hx.gy --proxy-port=1080
#composer镜像
{
    "repositories": [
        { "packagist": false },
        {
            "type": "composer",
            "url": "http://composer-proxy.jp/proxy/packagist"
        }
    ]
}
#npm
npm config set registry https://registry.npm.taobao.org 
#brew
cd /usr/local/
git remote set-url origin http://mirrors.ustc.edu.cn/homebrew.git
brew update
