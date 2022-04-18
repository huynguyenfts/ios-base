# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

def coreLibs
  use_frameworks!
  # Rx Extensions
  pod 'RxGesture'
  pod 'RxSwift'
  pod 'RxCocoa'
  pod 'RxDataSources', '~> 5.0'

  # Networking
  pod 'Moya/RxSwift'

  # Keyboard
  pod 'IQKeyboardManagerSwift'

  # Image
  pod 'Kingfisher', :git => 'https://github.com/onevcat/Kingfisher.git', :branch => 'version6-xcode13'
  
  # Extension
  pod 'SwifterSwift'
  
  # Tool
  pod 'R.swift'
  pod 'SwiftLint'

  # UI
  pod 'SVProgressHUD'
  pod 'Cosmos', '~> 23.0'
  pod 'MBProgressHUD', '~> 1.2'
  pod 'SnapKit', '~> 5.0'
  pod 'KafkaRefresh'
  pod 'SkeletonView'

end


target 'ios-base' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  coreLibs

  target 'ios-baseTests' do
    inherit! :search_paths
    coreLibs
  end

  target 'ios-baseUITests' do
    coreLibs
  end
  
  post_install do |installer_representation|
      installer_representation.pods_project.targets.each do |target|
          target.build_configurations.each do |config|
              config.build_settings['ALWAYS_EMBED_SWIFT_STANDARD_LIBRARIES'] = '$(inherited)'
          end
      end
  end
  
end
