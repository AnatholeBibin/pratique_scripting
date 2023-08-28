node{
def app
stage('Clone"){
checkout scm
}
stage ('Build image'){
  app = docker.build("monimage_script")
}
stage ('Run image' )
  docker.image(*monimage_script*).withRun('-p5000:5000"){c->
  sh 'docker ps'
  sh 'curl localhost'
}
}
