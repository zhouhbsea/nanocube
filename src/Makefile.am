#EXTRA_DATA = extra
#extradir = $(prefix)/bin
#extra_DATA = ncbuild

install-exec-hook:
	cp $(top_srcdir)/src/ncbuild $(prefix)/bin
	chmod +x $(prefix)/bin/ncbuild

AUTOMAKE_OPTIONS = subdir-objects

bin_PROGRAMS =        \
ncdmp                 \
ncserve               \
nc_q20_q20_u2_u4      \
nc_q25_q25_u2_u4      \
nc_q25_u2_u4          \
nc_q25_c1_u2_u4       \
nc_q25_c1_c1_u2_u4    \
nc_q25_c1_c1_c1_u2_u4

# AM_CPPFLAGS = -I$(top_srcdir)/src
AM_CXXFLAGS = -D_GLIBCXX_USE_NANOSLEEP -D_GLIBCXX_USE_SCHED_YIELD

ncdmp_SOURCES =       \
ncdmp.cc              \
ncdmp_base.cc         \
ncdmp_base.hh         \
TimeBinFunction.cc    \
TimeBinFunction.hh    \
DumpFile.cc           \
DumpFile.hh           \
MercatorProjection.cc \
MercatorProjection.hh

ncserve_SOURCES =     \
ncserve.cc            \
DumpFile.cc           \
DumpFile.hh

nc_SOURCES = \
Common.cc                 \
Common.hh                 \
ContentHolder.hh          \
DumpFile.cc               \
DumpFile.hh               \
FlatTree.hh               \
MemoryUtil.cc             \
MemoryUtil.hh             \
MercatorProjection.cc     \
MercatorProjection.hh     \
NanoCube.hh               \
NanoCubeInsert.hh         \
NanoCubeQuery.hh          \
NanoCubeQueryException.cc \
NanoCubeQueryException.hh \
NanoCubeQueryResult.hh    \
NanoCubeQueryResult.cc    \
NanoCubeSummary.hh        \
NanoCubeSummary.cc        \
NanoCubeReportBuilder.hh  \
NanoCubeSchema.cc         \
NanoCubeSchema.hh         \
NanoCubeTimeQuery.hh      \
QuadTree.cc               \
QuadTree.hh               \
QuadTreeNode.cc           \
QuadTreeNode.hh           \
QuadTreeUtil.hh           \
Query.cc                  \
Query.hh                  \
QueryParser.cc            \
QueryParser.hh            \
QueryResult.cc            \
QueryResult.hh            \
Report.cc                 \
Report.hh                 \
json.cc                   \
json.hh                   \
maps.cc                   \
maps.hh                   \
geometry.cc               \
geometry.hh               \
Server.cc                 \
Server.hh		  \
Stopwatch.cc              \
Stopwatch.hh              \
Stopwatch.hh              \
TaggedPointer.hh          \
TimeBinFunction.cc        \
TimeBinFunction.hh        \
TimeSeries.cc             \
TimeSeries.hh             \
TimeSeriesEntryType.hh    \
Tuple.hh                  \
Util.cc                   \
Util.hh                   \
vector.cc                 \
vector.hh                 \
mongoose.c                \
nc.cc                     \
small_vector.hh           \
qtfilter.hh               \
qtfilter.cc               \
geom2d/base.cc            \
geom2d/base.hh		  \
geom2d/boundingbox.cc	  \
geom2d/boundingbox.hh	  \
geom2d/geom2d.hh	  \
geom2d/make_monotone.cc	  \
geom2d/make_monotone.hh	  \
geom2d/planegraph.cc      \
geom2d/planegraph.hh	  \
geom2d/point.cc		  \
geom2d/point.hh		  \
geom2d/polygon.cc         \
geom2d/polygon.hh	  \
geom2d/tile.cc		  \
geom2d/tile.hh 

VERSION = $(shell cat $(top_srcdir)/VERSION)
AM_CXXFLAGS += -DVERSION=\"$(VERSION)\"

# NC_LIBS = -ldl -lpthread -lboost_thread -lboost_system
NC_LIBS = -ldl -lpthread -lboost_thread-mt -lboost_system-mt

nc_q20_q20_u2_u4_LDFLAGS  = $(NC_LIBS)
nc_q20_q20_u2_u4_CXXFLAGS = \
    -D_GLIBCXX_USE_NANOSLEEP \
    -D_GLIBCXX_USE_SCHED_YIELD \
    -DLIST_DIMENSION_NAMES=q20,q20 \
    -DLIST_VARIABLE_TYPES=u2,u4 \
    -DVERSION=\"$(VERSION)\"
nc_q20_q20_u2_u4_SOURCES =\
    $(nc_SOURCES)

nc_q25_q25_u2_u4_LDFLAGS  = $(NC_LIBS)
nc_q25_q25_u2_u4_CXXFLAGS = \
    -D_GLIBCXX_USE_NANOSLEEP \
    -D_GLIBCXX_USE_SCHED_YIELD \
    -DLIST_DIMENSION_NAMES=q25,q25 \
    -DLIST_VARIABLE_TYPES=u2,u4 \
    -DVERSION=\"$(VERSION)\"
nc_q25_q25_u2_u4_SOURCES =\
    $(nc_SOURCES)

nc_q25_u2_u4_LDFLAGS  = $(NC_LIBS)
nc_q25_u2_u4_CXXFLAGS = \
    -D_GLIBCXX_USE_NANOSLEEP \
    -D_GLIBCXX_USE_SCHED_YIELD \
    -DLIST_DIMENSION_NAMES=q25 \
    -DLIST_VARIABLE_TYPES=u2,u4 \
    -DVERSION=\"$(VERSION)\"
nc_q25_u2_u4_SOURCES =\
    $(nc_SOURCES)

nc_q25_c1_u2_u4_LDFLAGS  = $(NC_LIBS)
nc_q25_c1_u2_u4_CXXFLAGS = \
    -D_GLIBCXX_USE_NANOSLEEP \
    -D_GLIBCXX_USE_SCHED_YIELD \
    -DLIST_DIMENSION_NAMES=q25,c1 \
    -DLIST_VARIABLE_TYPES=u2,u4 \
    -DVERSION=\"$(VERSION)\"
nc_q25_c1_u2_u4_SOURCES =\
    $(nc_SOURCES)

nc_q25_c1_c1_u2_u4_LDFLAGS  = $(NC_LIBS)
nc_q25_c1_c1_u2_u4_CXXFLAGS = \
    -D_GLIBCXX_USE_NANOSLEEP \
    -D_GLIBCXX_USE_SCHED_YIELD \
    -DLIST_DIMENSION_NAMES=q25,c1,c1 \
    -DLIST_VARIABLE_TYPES=u2,u4 \
    -DVERSION=\"$(VERSION)\"
nc_q25_c1_c1_u2_u4_SOURCES =\
    $(nc_SOURCES)

nc_q25_c1_c1_c1_u2_u4_LDFLAGS  = $(NC_LIBS)
nc_q25_c1_c1_c1_u2_u4_CXXFLAGS = \
    -D_GLIBCXX_USE_NANOSLEEP \
    -D_GLIBCXX_USE_SCHED_YIELD \
    -DLIST_DIMENSION_NAMES=q25,c1,c1,c1 \
    -DLIST_VARIABLE_TYPES=u2,u4 \
    -DVERSION=\"$(VERSION)\"
nc_q25_c1_c1_c1_u2_u4_SOURCES =\
    $(nc_SOURCES)
