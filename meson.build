project('MainCallChecker', 'cpp')

cxx = meson.get_compiler('cpp')

# from https://github.com/mesonbuild/meson/issues/1899
dep_llvm = dependency('llvm', version: '>= 6.0.0')
llvm_libdir = dep_llvm.get_configtool_variable('libdir')
dep_libs = [
	cxx.find_library('clangAnalysis', dirs : llvm_libdir),
	cxx.find_library('clangAST', dirs : llvm_libdir),
	cxx.find_library('clangStaticAnalyzerCore', dirs : llvm_libdir),
	cxx.find_library('LLVM', dirs : llvm_libdir)
]

library('MainCallChecker', 'MainCallChecker.cpp', dependencies: dep_libs)