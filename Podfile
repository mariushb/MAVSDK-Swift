platform :ios, '11.0'

target 'MAVSDK_Swift' do
  use_frameworks!

  $rxVersion = 'https://github.com/ReactiveX/RxSwift.git'

  # Pods for Dronecode-SDK-Swift
  pod 'SwiftGRPC', :git => 'https://github.com/JonasVautherin/grpc-swift.git'
  pod 'RxSwift', :git => $rxVersion

  target 'MAVSDK_SwiftTests' do
    inherit! :search_paths
    # Pods for testing
    pod 'RxBlocking', :git => $rxVersion
    pod 'RxTest', :git => $rxVersion
  end

  target 'MAVSDK_SwiftIntegrationTests' do
    inherit! :search_paths
    # Pods for testing
    pod 'RxBlocking', :git => $rxVersion
    pod 'RxTest', :git => $rxVersion
  end
end

post_install do |installer_representation|
  installer_representation.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['ONLY_ACTIVE_ARCH'] = 'NO'
    end
  end
end
