#Change thos line to a different location if needed
ESSENS=/Users/sanjuktabhowmick/STARyNET/GoldenBox/ESSENS
#ESSENS= ./ESSENS

CXX=g++-8
CXXFLAGS=-g -fopenmp 


#Including BASIC_IO
BASIC_IO= $(ESSENS)/Core/Basic_IO

BASIC_IO_PREPROCESS=$(BASIC_IO)/PreProcess

BASIC_IO_FORMAT=$(BASIC_IO)/Format
BASIC_IO_FORMAT_INPUT=$(BASIC_IO_FORMAT)/Input
BASIC_IO_FORMAT_OUTPUT=$(BASIC_IO_FORMAT)/Output

BASIC_IO_INC=-I $(BASIC_IO_PREPROCESS)/Exceptions\
 -I $(BASIC_IO_PREPROCESS)/Level0 \
 -I $(BASIC_IO_PREPROCESS)/Level1 \
 -I $(BASIC_IO_PREPROCESS)/Level2 \
 -I $(BASIC_IO_FORMAT_INPUT_FORMAT)/Exceptions \
 -I $(BASIC_IO_FORMAT)/Level0/ \
 -I $(BASIC_IO_FORMAT_INPUT)/Level1/ -I $(BASIC_IO_FORMAT_INPUT)/Level2 \
-I $(BASIC_IO_FORMAT_OUTPUT)/Level1/ -I $(BASIC_IO_FORMAT_OUTPUT)/Level2 


BASIC_SETOP=$(ESSENS)/Core/Basic_SetOps

BASIC_SETOP_INC=-I $(BASIC_SETOP)/Level0 \
-I $(BASIC_SETOP)/Level1/ \
-I $(BASIC_SETOP)/Level2

BASIC_TRAVERSAL=$(ESSENS)/Core/Basic_Traversal

BASIC_TRAVERSAL_INC=-I$(BASIC_TRAVERSAL)/Level0 \
-I$(BASIC_TRAVERSAL)/Level1 \
-I$(BASIC_TRAVERSAL)/Level2

BASIC_CHANGE=$(ESSENS)/Basic_Change

BASIC_CHANGE_INC=-I$(BASIC_CHANGE)/Level0 \
-I$(BASIC_CHANGE)/Level1 \
-I$(BASIC_CHANGE)/Level2

BASIC_ANALYSIS=$(ESSENS)/Basic_Analysis
BASIC_ANALYSIS_INC=-I$(BASIC_ANALYSIS)/Level0

all: 	main_code.cpp      
	$(CXX) $(CXXFLAGS) $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) main_code.cpp
cE: 	create_edgelist.cpp
	$(CXX) -g -o cE.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) create_edgelist.cpp
sparse: sparsify.cpp
	$(CXX) -g  -o sparse.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) sparsify.cpp
tEx: 	traversalEx.cpp
	$(CXX) -g  -o tEx.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) traversalEx.cpp
bfs: 	BFS.cpp
	$(CXX) -g -o bfs.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) BFS.cpp
chChk: 	chordalchk.cpp
	$(CXX) -g -o chChk.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) chordalchk.cpp
lpath: 	longest_path.cpp
	$(CXX) -g -o lpath.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) longest_path.cpp

permF: 	permute_file.cpp
	$(CXX) -g -o permF.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) permute_file.cpp

BFS_try: BFS.cpp
	$(CXX) -g -fopenmp -o BFST.out $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) $(BASIC_CHANGE_INC) $(BASIC_ANALYSIS_INC) BFS.cpp
test1: 	test_SetOps.cpp
	$(CXX) $(BASIC_IO_INC) $(BASIC_SETOP_INC) $(BASIC_TRAVERSAL_INC) test_SetOps.cpp

clean:
	$(RM) *.out *.o
