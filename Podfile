# Uncomment the next line to define a global platform for your project
platform :ios, '13.0'

#source 'https://github.com/CocoaPods/Specs.git' Or better >> install! 'cocoapods', :warn_for_unused_master_specs_repo => false
#for >> [!] Your project does not explicitly specify the CocoaPods master specs repo. Since CDN is now used as the default, you may safely remove it from your repos directory via `pod repo remove master`. To suppress this warning please add `warn_for_unused_master_specs_repo => false` to your Podfile.
#source 'https://github.com/CocoaPods/Specs.git'
install! 'cocoapods', :warn_for_unused_master_specs_repo => false

target 'CI_CD_Tutorial' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  # Pods for CI_CD_Tutorial
  pod 'SkeletonView', '1.21.2'
  pod 'AllowX', '1.1.2'
  pod 'R.swift', '5.4.0'
  pod 'Alamofire', '5.4.3'
  pod 'IQKeyboardManagerSwift', '6.5.6'
  pod 'SwiftLint', '0.43.1'
  #pod 'Firebase/Auth', '8.5.0'
  #pod 'Firebase/Analytics', '8.5.0'
  #pod 'Firebase/Firestore', '8.5.0'
  pod 'lottie-ios', '3.2.3'
  pod 'Resolver', '1.4.3'
  pod 'JGProgressHUD', '2.2'
  pod 'Kingfisher', '7.1.1'

end


  ## Delete Modify target for warning and chnage to 9 if its 8
post_install do |pi|
   pi.pods_project.targets.each do |t|
       t.build_configurations.each do |bc|
           if bc.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] == '8.0'
             bc.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '9.0'
           end
       end
   end
end

  ## Delete target 
  # post_install do |installer|
  #   installer.pods_project.targets.each do |target|
  #     target.build_configurations.each do |config|
  #       config.build_settings.delete 'IPHONEOS_DEPLOYMENT_TARGET'
  #     end
  #   end
  # end
