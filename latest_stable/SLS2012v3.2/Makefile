TARGET = SLS2012v3

CPP_SRC = SLS2012v3.2/CameraController.cpp SLS2012v3.2/CameraCalibration.cpp SLS2012v3.2/GrayCodes.cpp SLS2012v3.2/MeshCreator.cpp SLS2012v3.2/PointCloudImage.cpp SLS2012v3.2/Projector.cpp SLS2012v3.2/Reconstructor.cpp SLS2012v3.2/Sample.cpp SLS2012v3.2/Scanner.cpp SLS2012v3.2/SLS2012.cpp SLS2012v3.2/Utilities.cpp SLS2012v3.2/VirtualCamera.cpp SLS2012v3.2/WebCam.cpp

OBJ = $(C_SRC:.c=.o) $(CPP_SRC:.cpp=.o)

#DEBUG	= -g -O0
DEBUG	= -O3
CC	= gcc
CXX = g++
LD = $(CXX)

CFLAGS = $(DEBUG) `pkg-config --cflags opencv`
LIBS = `pkg-config --libs opencv` -lncurses

all: $(TARGET)

$(TARGET): $(OBJ)
	@echo [link]
	$(LD) -o $@ $(OBJ) $(LDFLAGS) $(LDLIBS) $(LIBS)

.c.o:
	@echo [CC] $<
	$(CC) -c $(CFLAGS) $< -o $@

.cpp.o:
	@echo [CXX] $<
	$(CXX) -c $(CFLAGS) $< -o $@

clean:
	@echo "[Clean]"
	@rm -f $(OBJ) *~ core tags $(BINS) $(TARGET)
