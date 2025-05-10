
```

# build dynamic library with -fPIC -shared
CFLAGS   := -g # -O3 -fPIC # CXXFLAGS for .cpp
CPPFLAGS := -MMD -MP # -I../foo -DNDEBUG
LDFLAGS  := # -L../foo -shared -static
LDLIBS   := # -lfoo
#CC      := $(CXX) # link with CXX for .cpp

# target name is basename of one of the source files
main: $(patsubst %.c,%.o,$(wildcard *.c)) # .cpp
-include *.d
clean: ; $(RM) *.o *.d main
.PHONY: clean

# fully static link archive with -static
ARFLAGS := rvU
(%): % ;
%.a: ; $(AR) $(ARFLAGS) $@ $?
libfoo.a: libfoo.a($(patsubst %.c,%.o,$(wildcard *.c))) # .cpp

```


<!--
This is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

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
