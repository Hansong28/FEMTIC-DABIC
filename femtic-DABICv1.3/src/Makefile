CXX           = mpiicpc
CC            = mpiicpx  #oneapi 2025 
GCC           = mpigxx

# Default release option
CXXFLAGS      = -O3 \
                -qopenmp \
                -D_LINUX \
                -DMKL_ILP64 \
                -D_USE_OMP \
                -DNDEBUG \
		-diag-disable=10441

# debug option (added -g, changed to -O0)
DEBUG_CXXFLAGS = -g \
                -O0 \
                -qopenmp \
                -D_LINUX \
                -DMKL_ILP64 \
                -D_USE_OMP \
		-diag-disable=10441

DEST          = ./
LDFLAGS       =
LIBS          =  -lmkl_intel_ilp64 -lmkl_intel_thread -lmkl_core -lmkl_blacs_intelmpi_ilp64 -liomp5 -lpthread -lm -ldl

OBJS          = AnalysisControl.o \
                ComplexSparseMatrix.o \
                ComplexSparseSquareMatrix.o \
                ComplexSparseSquareSymmetricMatrix.o \
                ComplexSparseSquareUnsymmetricMatrix.o \
                DoubleSparseMatrix.o \
                DoubleSparseSquareMatrix.o \
                DoubleSparseSquareSymmetricMatrix.o \
                DoubleSparseSquareUnsymmetricMatrix.o \
                Forward2D.o \
                Forward2DQuadrilateralElement.o \
                Forward2DNonConformingQuadrilateralElement0thOrderEdgeBased.o \
                Forward2DQuadrilateralElementEdgeBased.o \
                Forward2DSquareElement.o \
                Forward2DSquareElement0thOrderEdgeBased.o \
                Forward2DSquareElement1stOrderEdgeBased.o \
                Forward2DSquareElement1stOrderNodeBased.o \
                Forward2DSquareElement2ndOrderNodeBased.o \
                Forward2DSquareElementEdgeBased.o \
                Forward2DSquareElementNodeBased.o \
                Forward2DTriangleElement.o \
                Forward2DTriangleElement0thOrderEdgeBased.o \
                Forward2DTriangleElement1stOrderNodeBased.o \
                Forward2DTriangleElementEdgeBased.o \
                Forward2DTriangleElementNodeBased.o \
                Forward3D.o \
                Forward3DBrickElement0thOrder.o \
                Forward3DNonConformingHexaElement0thOrder.o \
                Forward3DTetraElement0thOrder.o \
                Inversion.o \
                InversionGaussNewtonModelSpace.o \
		InversionGaussNewtonDataSpace.o \
		InversionGaussNewtonDataSpace_ABIC.o \
		main.o \
                MeshData.o \
                MeshDataBrickElement.o \
                MeshDataNonConformingHexaElement.o \
                MeshDataTetraElement.o \
                AdditinalOutputPoint.o \
                ObservedDataStation.o \
                ObservedDataStationPoint.o \
                ObservedDataStationMT.o \
                ObservedDataStationApparentResistivityAndPhase.o \
                ObservedDataStationHTF.o \
                ObservedDataStationVTF.o \
                ObservedDataStationPT.o \
                ObservedDataStationNMT.o \
                ObservedDataStationNMT2.o \
                ObservedDataStationNMT2ApparentResistivityAndPhase.o \
                ObservedData.o \
                OutputFiles.o \
                PARDISOSolver.o \
                PARDISOSolverComplex.o \
                PARDISOSolverDouble.o \
                ResistivityBlock.o \
                RougheningMatrix.o \
                RougheningSquareMatrix.o \
                Util.o
PROGRAM       = femtic-dabic

all:            $(PROGRAM)

# default: release mode
$(PROGRAM):     $(OBJS)
	$(CXX) $(CXXFLAGS) $(OBJS) $(LDFLAGS) $(LIBS) -o $(PROGRAM)

debug: CXXFLAGS = $(DEBUG_CXXFLAGS)
debug: $(PROGRAM)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -f *.o *~ $(PROGRAM)