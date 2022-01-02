CPMAddPackage(
	NAME date
	GITHUB_REPOSITORY HowardHinnant/date
	VERSION 3.0.1
	OPTIONS "BUILD_TZ_LIB ON" "USE_SYSTEM_TZ_DB ON"	
	)

add_executable(oracle oracle.cpp)
target_link_libraries(oracle project_options project_warnings date::date date::date-tz)
