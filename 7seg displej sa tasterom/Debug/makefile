################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
7seg\ displej\ sa\ tasterom.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
7seg\ displej\ sa\ tasterom.list \

OBJCOPY_HEX += \
7seg\ displej\ sa\ tasterom.hex \

OBJCOPY_BIN += \
7seg\ displej\ sa\ tasterom.bin \


# All Target
all: 7seg\ displej\ sa\ tasterom.elf secondary-outputs

# Tool invocations
7seg\ displej\ sa\ tasterom.elf: $(OBJS) $(USER_OBJS) C:\Users\Lazar\Desktop\7seg\ displej\ projekat\7seg\ displej\ sa\ tasterom\STM32F103C6UX_FLASH.ld
	arm-none-eabi-gcc -o "7seg displej sa tasterom.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Lazar\Desktop\7seg displej projekat\7seg displej sa tasterom\STM32F103C6UX_FLASH.ld" --specs=nosys.specs -Wl,-Map="7seg displej sa tasterom.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

7seg\ displej\ sa\ tasterom.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "7seg displej sa tasterom.list"
	@echo 'Finished building: $@'
	@echo ' '

7seg\ displej\ sa\ tasterom.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "7seg displej sa tasterom.hex"
	@echo 'Finished building: $@'
	@echo ' '

7seg\ displej\ sa\ tasterom.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "7seg displej sa tasterom.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
