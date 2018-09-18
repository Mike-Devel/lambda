cmake_minimum_required(VERSION 3.5)
project(boost-lambda)

add_library(boost_lambda INTERFACE)
add_library(Boost::lambda ALIAS boost_lambda)

target_include_directories(boost_lambda INTERFACE include)

target_link_libraries(boost_lambda
	INTERFACE
		Boost::bind
        Boost::config
		Boost::core
		Boost::detail
		Boost::iterator
		Boost::mpl
		Boost::preprocessor
        Boost::tuple
		Boost::type_traits
		Boost::utility
)

