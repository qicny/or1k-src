## Process this with automake to create Makefile.in

AUTOMAKE_OPTIONS = foreign

AM_CFLAGS = -Wall

noinst_PROGRAMS = rda

INCLUDES = -I$(srcdir) -I$(srcdir)/../include 

rda_SOURCES = server.c 
EXTRA_rda_SOURCES = linux-target.c solaris-target.c \
	ptrace-target.c dummy-target.c stock-breakpoints.c diagnostics.c
TARGET_MODULES = @TARGET_MODULES@
rda_LDADD = $(TARGET_MODULES) ../lib/librda.la
rda_DEPENDENCIES = $(server_OBJECTS) $(TARGET_MODULES) ../lib/librda.la
rda_LDFLAGS = -ldl -rdynamic
