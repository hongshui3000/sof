# SPDX-License-Identifier: BSD-3-Clause

add_local_sources(sof
	handler-ipc3.c
	helper-ipc3.c
	ipc-common.c
)

if (CONFIG_TRACE)
	add_local_sources(sof
		dma-copy.c)
endif()

if (CONFIG_LIBRARY)
	return()
endif()

if (CONFIG_HOST_PTABLE)
	add_local_sources(sof
		ipc-host-ptable.c)
endif()
