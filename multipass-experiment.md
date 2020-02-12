import os
# from cloudmesh.common.util import banner

class Provider:
    
    def __init__(self, name):
        self.name = name

    def list(self):
        os.system("multipass list")

    def find(self, str_match=""):
        os.system(f"multipass find {str_match}")

    def launch(self, image=""):
	    os.system(f"multipass launch {image}")

    def shell(self):
        os.system("multipass shell")

    def run(self, command):
        os.system(f"multipass exec {command}")
    
    def delete(self, inst_name):
        os.system(f"multipass delete {name}")

    def purge(self):
        os.system(f"multipass purge {command}")

if __name__ == "__main__":
    p = Provider("cloudmesh")
    p.find()
    p.list()
