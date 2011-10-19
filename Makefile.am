# 
# Install files into the same locations as does the corresponding
# ubuntu package.
#

bindir = /usr/bin
libdir = /usr/lib/ec2-api-tools/

toolsdir = ec2-api-tools-1.4.4.2

cpiop = find  . ! -regex '\(.*~\|.*\.bak\|.*\.cmd\|.*\.swp\|.*\#.*\#\)' -print0 | \
  cpio -0pd

install-exec-hook:
	mkdir -p $(DESTDIR)$(bindir)
	cd $(toolsdir)/bin; $(cpiop) $(DESTDIR)$(bindir)
	mkdir -p $(DESTDIR)$(libdir)
	cd $(toolsdir)/lib; $(cpiop) $(DESTDIR)$(libdir)



