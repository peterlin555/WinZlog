
# Updated: 15th August 2004

CC				=	como
CPPC			=	como
AR				=	lib

UNIXEM_INC_DIR	=	..\..\include
UNIXEM_LIB_DIR	=	..\..\lib
UNIXEM_OBJ_DIR	=	.
UNIXEM_SRC_DIR	=	..\..\src
CMP_ID			=	como4301


CC_ARGS			=	--no_version -c -w

CPPC_ARGS		=	--no_version -c -w

UNIXEM_LIB		=	$(UNIXEM_LIB_DIR)\unixem.$(CMP_ID).lib


OBJS_DEBUG		=	\
					$(UNIXEM_OBJ_DIR)\atomic.obj	\
					$(UNIXEM_OBJ_DIR)\dirent.obj	\
					$(UNIXEM_OBJ_DIR)\dlfcn.obj		\
					$(UNIXEM_OBJ_DIR)\glob.obj		\
					$(UNIXEM_OBJ_DIR)\mmap.obj		\
					$(UNIXEM_OBJ_DIR)\time.obj		\
					$(UNIXEM_OBJ_DIR)\unistd.obj	\
					\


OBJS_RELEASE	=	\


# rules					

{$(UNIXEM_SRC_DIR)}.cpp{$(UNIXEM_OBJ_DIR)}.obj:
	$(CPPC) $(CPPC_ARGS) -I$(UNIXEM_INC_DIR) -o $@ $<

{$(UNIXEM_SRC_DIR)}.c{$(UNIXEM_OBJ_DIR)}.obj:
	$(CC) $(CC_ARGS) -I$(UNIXEM_INC_DIR) -o $@ $<

# targets

target:			\
				$(UNIXEM_LIB)	\
				\


clean:
	@-if exist $(UNIXEM_OBJ_DIR)\*.obj del $(UNIXEM_OBJ_DIR)\*.obj
	@-if exist $(UNIXEM_LIB) del $(UNIXEM_LIB)


$(UNIXEM_LIB):	$(OBJS_DEBUG)
	$(AR) -out:$@ -nologo $(OBJS_DEBUG)
