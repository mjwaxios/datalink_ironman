CXXFLAGS  = -g -Wall
LDFLAGS =
GTKFLAGS = `gtkmm-config --cflags`
GTKLDFLAGS = `gtkmm-config --libs`

ifdef efence
LDFLAGS += -lstdc++-2-libc6.1-1-2.9.0 -lefence
endif

all: fun signaldump hextofile

signaldump: signaldump.cc
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) -o $@ $^ $(LDFLAGS)

fun: fun.cc
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) $(GTKFLAGS) $(GTKLDFLAGS) -o $@ $^ $(LDFLAGS)

clean:
	rm -f *.o fun signaldump hextofile
