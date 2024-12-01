# Embedded

<!---
<gcc/config/rs6000/eabi.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()          \
    do                                      \
      {                                     \
        builtin_define_std ("PPC");         \
        builtin_define ("__embedded__");    \
        builtin_assert ("system=embedded"); \
        builtin_assert ("cpu=powerpc");     \
        builtin_assert ("machine=powerpc"); \
        TARGET_OS_SYSV_CPP_BUILTINS ();     \
      }                                     \
    while (0)

<gcc/config/rs6000/eabisim.h> (14.2.0)

  #define TARGET_OS_CPP_BUILTINS()           \
    do                                       \
      {                                      \
        builtin_define_std ("PPC");          \
        builtin_define ("__embedded__");     \
        builtin_define ("__simulator__");    \
        builtin_assert ("system=embedded");  \
        builtin_assert ("system=simulator"); \
        builtin_assert ("cpu=powerpc");      \
        builtin_assert ("machine=powerpc");  \
        TARGET_OS_SYSV_CPP_BUILTINS ();      \
      }                                      \
    while (0)
--->