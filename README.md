# Ansible Playbook for Ruby on Rails with Capistrano deployment server preparation

## System dependencies

* Ansible version >= 2.0

## Configuration

group_vars/all.yml should exist and contain:

    ---

    common_packages:
      - sudo
      - htop
      - mc
      - curl
      - wget
      - git
      - apt-transport-https
      - ca-certificates
      - gnupg2
      - libmysqlclient-dev
      - python-setuptools # easy_install (necessary for install python pip)

    passenger_key_server: "hkp://keyserver.ubuntu.com:80"
    passenger_key_id: "561F9B9CAC40B2F7"

    ubuntu_release: trusty

    mysql_root_password: 'your_password'

    app_dir: '/srv/www/your_webapp'
    src_dir: '/home/user/path/to/your_webapp_src'


## Run instructions

ansible-playbook -i stage site.yml -u root

## License

Please refer to [LICENSE](LICENSE).
