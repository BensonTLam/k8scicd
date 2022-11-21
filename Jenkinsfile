node{
    def appName = 'k8scicd'
    def tag = "v_latest"
    def img = "bensonlam/hellonode"
    def imgWithTag = "${img}:${tag}"
    
    checkout scm

    stage '建立映像檔'
    sh("docker build -t ${imgWithTag} .")

    stage '放置映像檔'
    sh("docker push ${imgWithTag} ")
}
