cmake_minimum_required(VERSION 3.24)
project(AltbaseModule_junkcoin VERSION 0.1.5 LANGUAGES CXX)

if(NOT COMMAND altbase_register_node_coin)
  message(FATAL_ERROR "Load the Altbase native-core SDK before this module")
endif()
altbase_register_node_coin(junkcoin JunkCoin)
altbase_register_utxo_coin(junkcoin JunkCoin)
