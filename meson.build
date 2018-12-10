project('mstch', 
        'cpp', 
        version : '1.0.1', 
        license : 'MIT', 
        default_options : ['cpp_std=c++11']
)

boost_dep = dependency('boost')
inclocal = include_directories('include')
incsrc   = include_directories('src')
incsrcstate  = include_directories('src/state')
incsrcvisitor  = include_directories('src/visitor')

subdir('src')

mstch_lib = library('mstch', include_directories : [inclocal, incsrc, incsrcstate, incsrcvisitor], sources: mstch_src, dependencies: [boost_dep])
mstch_dep = declare_dependency(include_directories: [inclocal, incsrc, incsrcstate, incsrcvisitor], link_with: mstch_lib)
