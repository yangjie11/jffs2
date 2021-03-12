# RT-Thread building script for component

from building import *

cwd = GetCurrentDir()
src = Split('''
dfs_jffs2.c
porting.c

cyg/compress/src/adler32.c
cyg/compress/src/compress.c
cyg/compress/src/deflate.c
cyg/compress/src/infback.c
cyg/compress/src/inffast.c
cyg/compress/src/inflate.c
cyg/compress/src/inftrees.c
cyg/compress/src/trees.c
cyg/compress/src/uncompr.c
cyg/compress/src/zutil.c

cyg/crc/crc16.c
cyg/crc/crc32.c
cyg/crc/posix_crc.c
kernel/rbtree.c
src/build.c
src/compr.c
src/compr_rtime.c
src/compr_rubin.c
src/compr_zlib.c
src/debug.c
src/dir-ecos.c
src/erase.c
src/flashio.c
src/fs-ecos.c
src/gc.c
src/gcthread.c
src/malloc-ecos.c
src/nodelist.c
src/nodemgmt.c
src/read.c
src/readinode.c
src/scan.c
src/write.c
''')

CPPPATH = [cwd, cwd + '/include', cwd + '/src', cwd + '/cyg', cwd + '/kernel', cwd + '/cyg/compress']

group = DefineGroup('Filesystem', src, depend = ['RT_USING_DFS', 'PKG_USING_DFS_JFFS2'], CPPPATH = CPPPATH)

Return('group')
