
PROG_ROOT = ../..

AM_CFLAGS = -g -DTEST_FUNCTION -I${PROG_ROOT}/ -I${PROG_ROOT}/${PBS_MACH} --coverage

lib_LTLIBRARIES = libcommon_cmds.la

AM_LDFLAGS = @CHECK_LIBS@ ${lib_LTLIBRARIES}

check_PROGRAMS = test_common_cmds

libcommon_cmds_la_SOURCES = scaffolding.c ${PROG_ROOT}/common_cmds.c
libcommon_cmds_la_LDFLAGS = @CHECK_LIBS@ -shared -lgcov

test_common_cmds_SOURCES = test_common_cmds.c

check_SCRIPTS = ${PROG_ROOT}/../test/coverage_run.sh

TESTS = $(check_PROGRAMS) ${check_SCRIPTS}

CLEANFILES = *.gcno *.gcda *.gcov core *.lo
