PROG_ROOT = ../..

AM_CFLAGS = -g -DTEST_FUNCTION -I${PROG_ROOT}/ -I${PROG_ROOT}/${PBS_MACH} --coverage

lib_LTLIBRARIES = libPBSD_manage2.la

AM_LDFLAGS = @CHECK_LIBS@ ${lib_LTLIBRARIES}

check_PROGRAMS = test_PBSD_manage2

libPBSD_manage2_la_SOURCES = scaffolding.c ${PROG_ROOT}/PBSD_manage2.c
libPBSD_manage2_la_LDFLAGS = @CHECK_LIBS@ -shared -lgcov

test_PBSD_manage2_SOURCES = test_PBSD_manage2.c

check_SCRIPTS = ${PROG_ROOT}/../../test/coverage_run.sh

TESTS = ${check_PROGRAMS} ${check_SCRIPTS} 

CLEANFILES = *.gcno *.gcda *.gcov core *.lo
