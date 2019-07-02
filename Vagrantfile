# Returns true if `GUI` environment variable is set to a non-empty value.
# Defaults to false
def gui_enabled?
  !ENV.fetch('GUI', '').empty?
end

Vagrant.configure("2") do |config|
  config.vm.box = "mwrock/Windows2016"
  config.vm.provider 'virtualbox' do |v|
    v.gui = gui_enabled?
  end
end
