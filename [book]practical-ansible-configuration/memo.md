

debug 모듈 사용방법
```yaml
---
- name: "Ping moduel demo"
  gather_facts: false
  hosts: all
  
  tasks:
    - name: Run our original Ansible command
      ansible.builtin.debug: msg="Ansible is fun"
    - name: We also need to test connectivity
      ansible.builtin.ping:

# run
ansibe-playbook test.ymls i hosts.ini
```

엔서블 변수 조회
```shell
ansible -i hosts.ini mylaptop -m setup
```