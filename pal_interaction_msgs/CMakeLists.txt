cmake_minimum_required(VERSION 2.8.3)
project(pal_interaction_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_message_files(
  DIRECTORY msg
  FILES
    actiontag.msg
    ASRActivation.msg
    ASREvent.msg
    ASRLangModelMngmt.msg
    ASRLanguage.msg
    asrresult.msg
    ASRSrvRequest.msg
    ASRSrvResponse.msg
    ASRStatus.msg
    asrupdate.msg
    AudioDeviceDescription.msg
    AudioPlayerState.msg
    audiosignal.msg
    DirectionOfArrival.msg
    EnablingSoundLocalisation.msg
    TTSstate.msg
    VoiceActivity.msg
    WebGuiEvent.msg
)

add_service_files(
  DIRECTORY srv
  FILES
    ASRService.srv
    recognizerService.srv
    SoundLocalisationService.srv
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime)
