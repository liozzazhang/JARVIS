### JARVIS -- ops management system
_**This project rely on following ops library**_

    http://git.patsnap.com/devops/ops-libraries

_Step1_: add private pypi repo
    
    cat << EOF > ~/.pip/pip.conf
    [global]
    extra-index-url = http://pypi.zhihuiya.com/simple
    [install]
    trusted-host = pypi.zhihuiya.com
    EOF

_Step2_: install ops library

    pip install ops
    
_Step3_: run command

    python ecs/jarvis.py -p s-search-ac-solr -t ecs -e release -r cn-north-1 --details format=yaml
    
###**[optional]**
_You also can use cli to deploy your project_

_Step1_: install jarvis_ecs with pip

    pip install jarvis_ecs
    
_Step2_: run jarvis-ecs cli
    
    jarvis-ecs -p s-search-ac-solr -t ecs -e release -r cn-north-1 --details format=yaml,file=../apps