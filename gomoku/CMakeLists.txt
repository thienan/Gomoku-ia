﻿enable_language(CSharp)
project(gomoku)

cmake_minimum_required(VERSION 3.10)

file(GLOB_RECURSE SRC src/*.cs)

add_executable(pbrain-deepmind ${SRC})
target_compile_options(pbrain-deepmind PRIVATE "/langversion:6")

set_property(TARGET pbrain-deepmind PROPERTY VS_DOTNET_REFERENCES
    "Microsoft.CSharp"
    "PresentationCore"
    "PresentationFramework"
    "System"
	"System.Drawing"
    "System.Core"
    "System.Data"
    "System.Data.DataSetExtensions"
    "System.Xaml"
    "System.Xml"
    "System.Xml.Linq"
    "WindowsBase")