# Define the compiler
CXX = g++

# Compiler flags
CXXFLAGS = -Wall -std=c++11

# Build target executable
TARGET = librarian_program

# Add your source files here
SOURCES = main.cpp librarian.cpp member.cpp book.cpp

# Default rule
all: $(TARGET)

# Rule for building the target
$(TARGET): $(SOURCES)
    $(CXX) $(CXXFLAGS) $(SOURCES) -o $(TARGET)

# Clean rule
clean:
    rm -f $(TARGET) *.o
