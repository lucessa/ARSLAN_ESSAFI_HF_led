################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
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
Projet_Afficheur_Motif.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Projet_Afficheur_Motif.list \

OBJCOPY_BIN += \
Projet_Afficheur_Motif.bin \


# All Target
all: Projet_Afficheur_Motif.elf secondary-outputs

# Tool invocations
Projet_Afficheur_Motif.elf: $(OBJS) $(USER_OBJS) /Users/busraarslan/Desktop/Microcontroleur/Code/Workspace/Projet_Afficheur_Motif/STM32F051C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Projet_Afficheur_Motif.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"/Users/busraarslan/Desktop/Microcontroleur/Code/Workspace/Projet_Afficheur_Motif/STM32F051C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Projet_Afficheur_Motif.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Projet_Afficheur_Motif.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Projet_Afficheur_Motif.list"
	@echo 'Finished building: $@'
	@echo ' '

Projet_Afficheur_Motif.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Projet_Afficheur_Motif.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
