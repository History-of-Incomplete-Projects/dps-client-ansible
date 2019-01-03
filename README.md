ansible-playbook -i hosts/HOST -e '{"expect_apts": ["loool", "accountsservice/bionic,now 0.6.45-1ubuntu1 amd64 [installed]"]}' deliverables.yaml --user alanjm --ask-pass --ask-become-pass

ansible-playbook -c local -i hosts/HOST -e '{"expect_apts": ["loool", "accountsservice/bionic,now 0.6.45-1ubuntu1 amd64 [installed]"], "expect_pips": ["pip", "wheel"]}' deliverables.yaml --ask-become-pass