find_all_sources(. rendering_SRCS)
if(TARGET_POSIX)
  if(TARGET_RPI OR TARGET_AML)
    find_all_sources(gles system_SRCS)
  else()
    find_all_sources(gl system_SRCS)
  endif()
elseif(TARGET_WIN32)
  find_all_sources(dx system_SRCS)
endif()
add_sources(${rendering_SRCS} ${system_SRCS})
