```

# link library with -shared and executable with -pie
CFLAGS   = -fPIC -g # -O3 # CXXFLAGS for .cpp
CPPFLAGS = -MMD -MP # -I../foo -DNDEBUG
LDFLAGS  = -fsanitize=address # -L../foo -shared -pie
LDLIBS   = # -lfoo
#CC      = $(CXX) # link with CXX for .cpp

# target name is basename of one of the source files
main : $(patsubst %.c,%.o,$(wildcard *.c)) # .cpp
-include *.d
clean : ; -rm -fr *.o *.d main
.PHONY : clean

```

<!--
**ljhm/ljhm** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
 
Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
