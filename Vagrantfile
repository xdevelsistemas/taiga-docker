VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.define "postgres-env" do |v|
         v.vm.provider "docker" do |d|
           d.vagrant_vagrantfile = ENV['VAGRANT_MAIN_FILE']
           d.vagrant_machine = "core-01"
           d.env = {
             POSTGRES_PASSWORD: "postgres",
           }
           d.image = "xdevelsistemas/debian-env:postgresql-env"
           d.ports = ["5432:5432"]
           d.volumes = ["/home/core/data/postgres/data/postgresql:/var/lib/postgresql"]
          d.name = "postgres"
         end
    end
end





