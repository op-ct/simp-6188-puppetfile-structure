moduledir 'modules'

# ==============================================================================
# SIMP Puppetfiles
# ------------------------------------------------------------------------------
# Uncomment/comment the SIMP subsystems you want from the list below:
simp_puppetfiles = [
  'Puppetfile.core',      # SIMP's core modules **DO NOT DISABLE**
  'Puppetfile.nfs',       # NFS services and client
  'Puppetfile.docker',    # Docker managment
  # 'Puppetfile.elg5',     # Manage an ELG stack (deprecated)
  # 'Puppetfile.gitlab',   # Manage a GitLab server
]

simp_puppetfiles.each do |puppetfile|
  instance_eval(File.read("Puppetfiles/simp/#{puppetfile}"))
end
# ==============================================================================

# It is recommended to add Roles and Profiles under a `site/` modules directory
# at the top level of the environment directory/control repo.
#
# Further reading:
#
#   * https://github.com/puppetlabs/best-practices/blob/master/control-repo-contents.md
#   * https://puppet.com/docs/pe/latest/the_roles_and_profiles_method.html
#   * https://github.com/puppetlabs/best-practices/blob/master/puppet-code-abstraction-roles.md
#   * https://github.com/puppetlabs/best-practices/blob/master/puppet-code-abstraction-profiles.md
#
# If you prefer instead to manage your site using a separate site module, uncomment the
# following entry, replacing the URL with your site module's rpeository:
#
# mod 'simp-site',
#  :git => 'https://github.com/simp/pupmod-simp-site'

Dir['Puppetfiles/site/Puppetfile*'].each do |puppetfile|
  instance_eval(File.read(puppetfile))
end
