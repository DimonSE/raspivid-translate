
add_definitions(-Werror)

# vcfiled - serves files to videocore. used for media handlers from
# OpenMAX/IL and loading VLLs.

# library to check if vcfiled is running or not
add_library(vcfiled_check vcfiled_check.c)

install(TARGETS vcfiled_check DESTINATION lib)
