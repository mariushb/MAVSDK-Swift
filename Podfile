`platform :ios, '9.0'

target 'MAVSDK_Swift' do
use_frameworks!

$gRPCVersion = '>= 0.4.2'
$rxVersion = '>= 4.0'



pod 'SwiftGRPC', $gRPCVersion
pod 'RxSwift', $rxVersion

target 'MAVSDK_SwiftTests' do
inherit! :search_paths
# Pods for testing
pod 'RxBlocking', $rxVersion
pod 'RxTest', $rxVersion
end

target 'MAVSDK_SwiftIntegrationTests' do
inherit! :search_paths
# Pods for testing
pod 'RxBlocking', $rxVersion
pod 'RxTest', $rxVersion
end
end

post_install do |installer_representation|
installer_representation.pods_project.targets.each do |target|
target.build_configurations.each do |config|
config.build_settings['ONLY_ACTIVE_ARCH'] = 'NO'
end
end
end
