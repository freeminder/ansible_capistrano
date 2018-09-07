# Ansible Playbook for Ruby on Rails with Capistrano deployment server preparation

## System dependencies

* Ansible version >= 2.0

## Configuration

* Remove extenstion '.example' from *group_vars/all.yml.example* file and edit its contents for your own usage.
* Replace IP address in *stage* file with yours server IP.

## Run instructions for Phusion Passenger app server with MySQL db:

    ansible-playbook -i stage passenger_mysql.yml -u root

## Run instructions for Puma app server with PostgreSQL db:

    ansible-playbook -i stage puma_postgresql.yml -u root

## License

Please refer to [LICENSE](LICENSE).
