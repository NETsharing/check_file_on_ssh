def verify_path(id, path):
    time.sleep(0.005)
    ssh = paramiko.SSHClient()
    ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())
    ssh.connect(host, username, password)
    stdin, stdout, stderr = ssh.exec_command(f'test -f {path} && echo $?')
    data = stdout.read() + stderr.read()
    ssh.close()
    if data:
        print('exist')
        return True
    else:

        return False
